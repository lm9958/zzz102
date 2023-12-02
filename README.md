# zzz102
p
import discord
from discord.ext import commands

bot = commands.Bot(command_prefix='!')

@bot.command()
async def server_info(ctx, server_link):
                parsed_link = discord.utils.parse_invite(server_link)
    server = await bot.fetch_guild(parsed_link.guild.id)
    server_name = server.name
    server_id = server.id
    await ctx.send(f"该服务器的名称为: {server_name}，ID为：{server_id}")

