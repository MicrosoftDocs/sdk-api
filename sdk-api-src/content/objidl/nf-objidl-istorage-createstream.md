---
UID: NF:objidl.IStorage.CreateStream
title: IStorage::CreateStream (objidl.h)
author: windows-sdk-content
description: Creates and opens a stream object with the specified name contained in this storage object.
old-location: stg\istorage_createstream.htm
tech.root: Stg
ms.assetid: 168f5ac9-8a72-4356-82a4-de3a7ec72c05
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateStream, CreateStream method [Structured Storage], CreateStream method [Structured Storage],IStorage interface, IStorage interface [Structured Storage],CreateStream method, IStorage.CreateStream, IStorage::CreateStream, _stg_istorage_createstream, objidl/IStorage::CreateStream, stg.istorage_createstream
ms.topic: method
req.header: objidl.h
req.include-header: 
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
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IStorage.CreateStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStorage::CreateStream


## -description


The <b>CreateStream</b> method
			 creates and opens a stream object with the specified name contained in this storage object. All elements within a storage objects, both streams and other storage objects, are kept in the same name space.


## -parameters




### -param pwcsName [in]

A pointer to a wide character null-terminated Unicode string that contains the name of the newly created stream. The name can be used later to open or reopen the stream. The name must not exceed 31 characters in length, not including the string terminator. The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE. This is a compound file restriction, not a structured storage restriction.


### -param grfMode [in]

Specifies the access mode to use when opening the newly created stream. For more information and descriptions of the possible values, see <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM Constants</a>.


### -param reserved1 [in]

Reserved for future use; must be zero.


### -param reserved2 [in]

Reserved for future use; must be zero.


### -param ppstm [out]

On return, pointer to the location of the new 
<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface pointer. This is only valid if the operation is successful. When an error occurs, this parameter is set to <b>NULL</b>.


## -returns



This method can return one of these values.




## -remarks



If a stream with the name specified in the <i>pwcsName</i> parameter already exists and the <i>grfMode</i> parameter includes the STGM_CREATE flag, the existing stream is replaced by a newly created one. Both the destruction of the old stream and the creation of the new stream object are subject to the transaction mode on the parent storage object.

The COM-provided compound file implementation of the <b>IStorage::CreateStream</b> method does not support the following behaviors:

<ul>
<li>The STGM_DELETEONRELEASE flag is not supported.</li>
<li>Transacted mode (STGM_TRANSACTED) is not supported for stream objects.</li>
<li>Opening the same stream more than once from the same storage is not supported. The STGM_SHARE_EXCLUSIVE sharing-mode flag must be specified in the <i>grfMode</i> parameter.</li>
</ul>
If the stream already exists and <i>grfMode</i> is set to STGM_FAILIFTHERE, this method fails with the return value STG_E_FILEALREADYEXISTS.




## -see-also




<a href="https://msdn.microsoft.com/2a2253f6-d3d3-403e-a9ba-53a541c7a31e">IStorage - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/f7bd1f26-e9a3-415d-8cd3-dc34f7ad8feb">IStorage::OpenStream</a>



<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>
 

 

