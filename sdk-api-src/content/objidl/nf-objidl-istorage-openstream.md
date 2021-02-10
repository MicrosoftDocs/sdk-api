---
UID: NF:objidl.IStorage.OpenStream
title: IStorage::OpenStream (objidl.h)
description: Opens an existing stream object within this storage object in the specified access mode.
helpviewer_keywords: ["IStorage interface [Structured Storage]","OpenStream method","IStorage.OpenStream","IStorage::OpenStream","OpenStream","OpenStream method [Structured Storage]","OpenStream method [Structured Storage]","IStorage interface","_stg_istorage_openstream","objidl/IStorage::OpenStream","stg.istorage_openstream"]
old-location: stg\istorage_openstream.htm
tech.root: Stg
ms.assetid: f7bd1f26-e9a3-415d-8cd3-dc34f7ad8feb
ms.date: 12/05/2018
ms.keywords: IStorage interface [Structured Storage],OpenStream method, IStorage.OpenStream, IStorage::OpenStream, OpenStream, OpenStream method [Structured Storage], OpenStream method [Structured Storage],IStorage interface, _stg_istorage_openstream, objidl/IStorage::OpenStream, stg.istorage_openstream
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStorage::OpenStream
 - objidl/IStorage::OpenStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IStorage::OpenStream
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

Specifies the access mode to be assigned to the open stream. For more information and descriptions of possible values, see <a href="/windows/desktop/Stg/stgm-constants">STGM Constants</a>.  Other modes you choose must at least specify STGM_SHARE_EXCLUSIVE when calling this method in the compound file implementation.

### -param reserved2 [in]

Reserved for future use; must be zero.

### -param ppstm [out]

A pointer to 
<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> pointer variable that receives the interface pointer to the newly opened stream object. If an error occurs, *<i>ppstm</i> must be set to <b>NULL</b>.

## -returns

This method can return one of these values.

## -remarks

<b>IStorage::OpenStream</b> opens an existing stream object within this storage object in the access mode specified in <i>grfMode</i>. There are restrictions on the permissions that can be given in <i>grfMode</i>. For example, the permissions on this storage object restrict the permissions on its streams. In general, access restrictions on streams need to be stricter than those on their parent storages. Compound-file streams must be opened with STGM_SHARE_EXCLUSIVE.

## -see-also

<a href="/windows/desktop/Stg/istorage-compound-file-implementation">IStorage - Compound File Implementation</a>



<a href="/windows/desktop/api/objidl/nf-objidl-istorage-createstream">IStorage::CreateStream</a>



<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>

