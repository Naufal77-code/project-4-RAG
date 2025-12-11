# Workflow RAG Progress 4 (n8n)

Repository ini berisi workflow n8n untuk proses:
- Mengambil file dari Google Drive
- Mengembangkannya menjadi embedding menggunakan OpenAI
- Melakukan chunking dengan text splitter
- Menyimpan embedding ke Pinecone Vector Store

## Struktur File
- `workflow.json` — file workflow n8n lengkap
- `README.md` — dokumentasi singkat workflow

## Alur Workflow
1. **Manual Trigger**  
   Memulai proses saat tombol "Execute Workflow" ditekan.

2. **Search Files (Google Drive)**  
   Mencari file pada folder spesifik di Google Drive.

3. **Download File**  
   Mengambil file dalam bentuk *binary*.

4. **Default Data Loader**  
   Mengubah file menjadi dokumen yang bisa diolah RAG.

5. **Recursive Text Splitter**  
   Memecah dokumen menjadi chunk.

6. **OpenAI Embeddings**  
   Membuat embedding vektor berukuran 1536 dimensi.

7. **Pinecone Vector Store**  
   Menyimpan embedding dan metadata ke Pinecone Index.

## Dependencies
- Google Drive OAuth2 Credential
- OpenAI API Key
- Pinecone API Key & Index (dimensi 1536)

## Catatan
Workflow ini berjalan di n8n self-hosted (Docker), sesuai Progress 4.
