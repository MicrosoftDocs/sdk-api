---
UID: NE:objidl.tagTYMED
title: tagTYMED
author: windows-sdk-content
description: Indicates the type of storage medium being used in a data transfer. They are used in the STGMEDIUM or FORMATETC structures.
old-location: com\tymed.htm
old-project: com
ms.assetid: ac41286f-7c67-444a-81b7-21b61079bbf5
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: TYMED, TYMED enumeration [COM], TYMED_ENHMF, TYMED_FILE, TYMED_GDI, TYMED_HGLOBAL, TYMED_ISTORAGE, TYMED_ISTREAM, TYMED_MFPICT, TYMED_NULL, _ole_TYMED, com.tymed, objidl/TYMED, objidl/TYMED_ENHMF, objidl/TYMED_FILE, objidl/TYMED_GDI, objidl/TYMED_HGLOBAL, objidl/TYMED_ISTORAGE, objidl/TYMED_ISTREAM, objidl/TYMED_MFPICT, objidl/TYMED_NULL, tagTYMED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidlbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TYMED
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ObjIdl.h
api_name:
 - TYMED
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagTYMED enumeration


## -description


Indicates the type of storage medium being used in a data transfer. They are used in the <a href="https://msdn.microsoft.com/5d05819a-10db-4d8e-91e4-8a7c05885cde">STGMEDIUM</a> or <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structures.


## -enum-fields




### -field TYMED_HGLOBAL

The storage medium is a global memory handle (<b>HGLOBAL</b>). Allocate the global handle with the GMEM_MOVEABLE flag. If the <b>punkForRelease</b> member of <a href="https://msdn.microsoft.com/5d05819a-10db-4d8e-91e4-8a7c05885cde">STGMEDIUM</a> is <b>NULL</b>, the destination process should use <a href="https://msdn.microsoft.com/5fe910ac-f857-45ca-9c0f-4f9ba3c5e61b">GlobalFree</a> to release the memory.


### -field TYMED_FILE

The storage medium is a disk file identified by a path. If the <a href="https://msdn.microsoft.com/5d05819a-10db-4d8e-91e4-8a7c05885cde">STGMEDIUM</a> <b>punkForRelease</b> member is <b>NULL</b>, the destination process should use <a href="https://msdn.microsoft.com/800f4d40-252a-44fe-b10d-348c22d69355">OpenFile</a> to delete the file.


### -field TYMED_ISTREAM

The storage medium is a stream object identified by an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> pointer. Use <a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">ISequentialStream::Read</a> to read the data. If the <a href="https://msdn.microsoft.com/5d05819a-10db-4d8e-91e4-8a7c05885cde">STGMEDIUM</a> <b>punkForRelease</b> member is not <b>NULL</b>, the destination process should use <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> to release the stream component.


### -field TYMED_ISTORAGE

The storage medium is a storage component identified by an <a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> pointer. The data is in the streams and storages contained by this <b>IStorage</b> instance. If the <a href="https://msdn.microsoft.com/5d05819a-10db-4d8e-91e4-8a7c05885cde">STGMEDIUM</a> <b>punkForRelease</b> member is not <b>NULL</b>, the destination process should use <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> to release the storage component.


### -field TYMED_GDI

The storage medium is a GDI component (<b>HBITMAP</b>). If the <a href="https://msdn.microsoft.com/5d05819a-10db-4d8e-91e4-8a7c05885cde">STGMEDIUM</a> <b>punkForRelease</b> member is <b>NULL</b>, the destination process should use <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> to delete the bitmap.


### -field TYMED_MFPICT

The storage medium is a metafile (<b>HMETAFILE</b>). Use the GDI functions to access the metafile's data. If the <a href="https://msdn.microsoft.com/5d05819a-10db-4d8e-91e4-8a7c05885cde">STGMEDIUM</a> <b>punkForRelease</b> member is <b>NULL</b>, the destination process should use <a href="https://msdn.microsoft.com/51766282-f185-4e29-a36e-1069d9d61f7c">DeleteMetaFile</a> to delete the bitmap.


### -field TYMED_ENHMF

The storage medium is an enhanced metafile. If the <a href="https://msdn.microsoft.com/5d05819a-10db-4d8e-91e4-8a7c05885cde">STGMEDIUM</a> <b>punkForRelease</b> member is <b>NULL</b>, the destination process should use <a href="https://msdn.microsoft.com/d3b93b3b-fa0b-4480-8348-19919c9e904d">DeleteEnhMetaFile</a> to delete the bitmap.


### -field TYMED_NULL

No data is being passed.



## -remarks



During data transfer operations, a storage medium is specified. This medium must be released after the data transfer operation. The provider of the medium indicates its choice of ownership scenarios in the value it provides in the <a href="https://msdn.microsoft.com/5d05819a-10db-4d8e-91e4-8a7c05885cde">STGMEDIUM</a> structure. A <b>NULL</b> value for the <b>pUnkForRelease</b> member indicates that the receiving body of code owns and can free the medium. A non-<b>NULL</b> pointer specifies that <a href="https://msdn.microsoft.com/da7d7bcb-0b5b-4053-8f0e-ff311c424375">ReleaseStgMedium</a> can always be called to free the medium.




## -see-also




<a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a>



<a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a>



<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>



<a href="https://msdn.microsoft.com/b5ef85d0-b54e-4831-87f1-ac6763179181">IOleCache</a>



<a href="https://msdn.microsoft.com/da7d7bcb-0b5b-4053-8f0e-ff311c424375">ReleaseStgMedium</a>



<a href="https://msdn.microsoft.com/5d05819a-10db-4d8e-91e4-8a7c05885cde">STGMEDIUM</a>
 

 

