---
UID: NF:objidl.IStorage.OpenStream
title: IStorage::OpenStream
author: windows-sdk-content
description: Opens an existing stream object within this storage object in the specified access mode.
old-location: stg\istorage_openstream.htm
old-project: Stg
ms.assetid: f7bd1f26-e9a3-415d-8cd3-dc34f7ad8feb
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IStorage interface [Structured Storage],OpenStream method, IStorage.OpenStream, IStorage::OpenStream, OpenStream, OpenStream method [Structured Storage], OpenStream method [Structured Storage],IStorage interface, _stg_istorage_openstream, objidl/IStorage::OpenStream, stg.istorage_openstream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IStorage.OpenStream
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IStorage::OpenStream


## -description


The <b>OpenStream</b> method
			 opens an existing stream object within this storage object in the specified access mode.


## -parameters




### -param pwcsName [in]

A pointer to a wide character null-terminated Unicode string that contains the name of the stream to open. The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE. This is a compound file restriction, not a structured storage restriction.


### -param reserved1 [in]

Reserved for future use; must be <b>NULL</b>.


### -param grfMode [in]

Specifies the access mode to be assigned to the open stream. For more information and descriptions of possible values, see <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM Constants</a>.  Other modes you choose must at least specify STGM_SHARE_EXCLUSIVE when calling this method in the compound file implementation.


### -param reserved2 [in]

Reserved for future use; must be zero.


### -param ppstm [out]

A pointer to 
<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> pointer variable that receives the interface pointer to the newly opened stream object. If an error occurs, *<i>ppstm</i> must be set to <b>NULL</b>.


## -returns



This method can return one of these values.




## -remarks



<b>IStorage::OpenStream</b> opens an existing stream object within this storage object in the access mode specified in <i>grfMode</i>. There are restrictions on the permissions that can be given in <i>grfMode</i>. For example, the permissions on this storage object restrict the permissions on its streams. In general, access restrictions on streams need to be stricter than those on their parent storages. Compound-file streams must be opened with STGM_SHARE_EXCLUSIVE.




## -see-also




<a href="https://msdn.microsoft.com/2a2253f6-d3d3-403e-a9ba-53a541c7a31e">IStorage - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/168f5ac9-8a72-4356-82a4-de3a7ec72c05">IStorage::CreateStream</a>



<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>
 

 

