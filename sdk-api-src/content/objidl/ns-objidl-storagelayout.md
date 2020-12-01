---
UID: NS:objidl.tagStorageLayout
title: StorageLayout (objidl.h)
description: Describes a single block of data, including its name, location, and length.
helpviewer_keywords: ["StorageLayout","StorageLayout structure [Structured Storage]","_stg_storagelayout","objidl/StorageLayout","stg.storagelayout"]
old-location: stg\storagelayout.htm
tech.root: Stg
ms.assetid: 1e4fb36d-077b-44bd-ab6e-8c122ec95a46
ms.date: 12/05/2018
ms.keywords: StorageLayout, StorageLayout structure [Structured Storage], _stg_storagelayout, objidl/StorageLayout, stg.storagelayout
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: StorageLayout
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagStorageLayout
 - objidl/tagStorageLayout
 - StorageLayout
 - objidl/StorageLayout
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objidl.h
api_name:
 - StorageLayout
---

# StorageLayout structure


## -description

The 
<b>StorageLayout</b> structure describes a single block of data, including its name, location, and length. To optimize a compound file, an application or layout tool passes an array of 
<b>StorageLayout</b> structures in a call to 
<a href="/windows/desktop/api/objidl/nf-objidl-ilayoutstorage-layoutscript">ILayoutStorage::LayoutScript</a>.

## -struct-fields

### -field LayoutType

The type of element to be written. Values are taken from the 
<a href="/windows/desktop/api/objidl/ne-objidl-stgty">STGTY</a> enumeration. <b>STGTY_STREAM</b> means read the block of data named by <b>pwcsElementName</b>. <b>STGTY_STORAGE</b> means open the storage specified in <b>pwcsElementName</b>. <b>STGTY_REPEAT</b> is used in multimedia applications to interface audio, video, text, and other elements. An opening <b>STGTY_REPEAT</b> value means that the elements that follow are to be repeated a specified number of times. The closing <b>STGTY_REPEAT</b> value marks the end of those elements that are to be repeated. Nested <b>STGTY_REPEAT</b> value pairs are permitted.

### -field pwcsElementName

The null-terminated Unicode string name of the storage or stream. If the element is a substorage or embedded object, the fully qualified storage path must be specified; for example,  "RootStorageName\SubStorageName\Substream".

### -field cOffset

Where the value of the <b>LayoutType</b> member is <b>STGTY_STREAM</b>, this flag specifies the beginning offset into the steam named in the <b>pwscElementName</b> member. 




Where <b>LayoutType</b> is <b>STGTY_STORAGE</b>, this flag should be set to zero.

Where <b>LayoutType</b> is <b>STGTY_REPEAT</b>, this flag should be set to zero.

### -field cBytes

Length, in bytes, of the data block named in <b>pwcsElementName</b>. 




Where <b>LayoutType</b> is <b>STGTY_STREAM</b>, <b>cBytes</b> specifies the number of bytes to read at <b>cOffset</b> from the stream named in <b>pwcsElementName</b>.

Where <b>LayoutType</b> is <b>STGTY_STORAGE</b>, this flag is ignored.

Where <b>LayoutType</b> is <b>STGTY_REPEAT</b>, a positive <b>cBytes</b> specifies the beginning of a repeat block. <b>STGTY_REPEAT</b> with zero <b>cBytes</b> marks the end of a repeat block.

A beginning block value of <b>STG_TOEND</b> specifies that elements in a following block are to be repeated after each stream has been completely read.

## -remarks

An array of 
<b>StorageLayout</b> structures might appear as follows.


```cpp
StorageLayout arrScript[]=
    // Read first 2k of "WordDocument" stream
    {STGTY_STREAM,L"WordDocument",{0,0},{0,2048}},
 
    //Test if "ObjectPool\88112233" storage exists
    {STGTY_STORAGE,L"ObjectPool\\88112233",{0,0},{0,0}},
 
    //Read 2k at offset 1048 of "WordDocument" stream
    {STGTY_STREAM,L"WordDocument",{0,10480},{0,2048}},
 
    //Interlace "Audio", "Video", and "Caption" streams
    {STGTY_REPEAT,NULL,0,STG_TOEND},
        {STGTY_STREAM,L"Audio", {0,0},{0,2048}},    // 2k of Audio
        {STGTY_STREAM,L"Video", {0,0},{0,65536}},   // 64k of Video
        {STGTY_STREAM,L"Caption", {0,0},{0,128}},   // 128b of text
    {STGTY_REPEAT,NULL, {0,0},{0,0}}
};
```


<div class="alert"><b>Note</b>  The parameters <i>cOffset</i> and <i>cBytes</i> are <b>LARGE_INTEGER</b> structures, used to represent a 64-bit signed integer value as a union of two 32-bit members. The two 32-bit members must be represented as a <b>LARGE_INTEGER</b> structure with <b>DWORD</b> LowPart and <b>LONG</b> HighPart as the structure members. (LowPart specifies the low-order 32 bits and HighPart specifies the high-order 32 bits.) If your compiler has built-in support for 64-bit integers, use the <b>QuadPart</b> member of the <b>LARGE_INTEGER</b> structure to store the 64-bit integer.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-ilayoutstorage-layoutscript">ILayoutStorage::LayoutScript</a>