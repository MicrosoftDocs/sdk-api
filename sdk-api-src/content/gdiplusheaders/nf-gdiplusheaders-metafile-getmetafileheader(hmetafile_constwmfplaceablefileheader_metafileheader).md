---
UID: NF:gdiplusheaders.Metafile.GetMetafileHeader(HMETAFILE,constWmfPlaceableFileHeader,MetafileHeader)
title: Metafile::GetMetafileHeader
description: The Metafile::GetMetafileHeader method gets the metafile header of this metafile.
tech.root: gdiplus
helpviewer_keywords: ["Metafile::GetMetafileHeader"]
ms.assetid: 5d12078c-4492-4bd1-a68b-8ff06dede784
ms.date: 05/20/2019
ms.keywords: Metafile::GetMetafileHeader
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdiplusheaders.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - Metafile::GetMetafileHeader
 - gdiplusheaders/Metafile::GetMetafileHeader
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusheaders.h
api_name:
 - Metafile::GetMetafileHeader
---

# Metafile::GetMetafileHeader(HMETAFILE,WmfPlaceableFileHeader*,MetafileHeader*)


## -description

The **Metafile::GetMetafileHeader** method gets the metafile header of this metafile.

## -parameters

### -param hWmf

Window handle to a metafile.

### -param wmfPlaceableFileHeader

Pointer to a placeable metafile header.

### -param header

Pointer to a <a href="/windows/desktop/api/gdiplusmetaheader/nl-gdiplusmetaheader-metafileheader">MetafileHeader</a> object that receives the copy of the metafile header.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>

<a href="/previous-versions/ms535294(v=vs.85)">Metafile::Metafile</a>

<a href="/windows/desktop/api/gdiplusmetaheader/nl-gdiplusmetaheader-metafileheader">MetafileHeader</a>

<a href="/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-metafiles-use">Loading and Displaying Metafiles</a>