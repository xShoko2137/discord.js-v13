const { Client, MessageEmbed} = require("discord.js");

const client = new Client({
    intents: 32767,
});
client.config = require("./config.json");
client.on("ready", async () => {
    console.log(`${client.user.username} smiga`)
})
client.on("messageCreate", async (message) => {
    if (message.author.bot ||!message.guild)return;
    if(message.content === "!embed") {
        const embed = new MessageEmbed()
        .setColor('#ffffff') /// ustawia kolor (hex color / https://discord.js.org/#/docs/main/stable/typedef/ColorResolvable)
        .setTitle('Tytuł') /// ustawia tytuł embeda 
        .setURL('https://dc.improveddiscord.pl/') /// Ustawia klikalny link na tytuł
        .setAuthor('Autor', 'https://i.imgur.com/AfFp7pu.png', 'https://dc.improveddiscord.pl/') /// Ustawia autora embed'a  Nazwa Autora/Link ikony / klikalny link na autora
        .setDescription('Tutaj wpisujesz opis')  //// Ustawia opis embeda 
        .setThumbnail('https://i.imgur.com/AfFp7pu.png') /// ustawia obrazek w prawym gównym rogu embeda
        .addFields(
            { name: 'Tutaj wpisujesz tytuł', value: 'Jakis opis pepeHey' },
        ) //// Name ustawia tytuł, value ustawia opis
        .addField('Inline field title', 'Some value here', true) /// pierwsza wartość ustawia tytuł druga opis, "true" jest odpowiedzialne za ustawienie pola w jednej linii (max 3 w jednej linii)
        .setImage('https://i.imgur.com/AfFp7pu.png') //// Ustawia obrazek w embedzie (MUSI TO BYĆ LINK)
        .setTimestamp() /// Ustawia date nadole w stopce, puste ustawia czas wyslania embed'a np. Wczoraj o 21;37
        .setFooter('Coś na stopce', 'https://i.imgur.com/AfFp7pu.png'); /// Pierwsze ustawia tekst na stopce, drugie odpowiedzialne jest za obrazek przy stopce

message.channel.send({ embeds: [embed] });
    }
})
client.login(client.config.token);
