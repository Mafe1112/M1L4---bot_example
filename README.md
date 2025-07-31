import discord
from discord.ext import commands 

bot = commands.Bot(commands_prefix="$")

@bot.event
async def on_ready():
    print(f"Conectado como {bot.user}")

@bot.command()
async def hola(ctx):
    await ctx.send("¡Hola!")

bot.run("TOKEN")
