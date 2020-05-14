---
UID: NF:gdiplusheaders.Metafile.GetMetafileHeader(IN HMETAFILE,IN const WmfPlaceableFileHeader,OUT MetafileHeader)
title: Metafile::GetMetafileHeader
description: The Metafile::GetMetafileHeader method gets the metafile header of this metafile.helpviewer_keywords: ["Metafile::GetMetafileHeader"]
ms.assetid: 5d12078c-4492-4bd1-a68b-8ff06dede784
ms.date: 05/20/2019
ms.keywords: Metafile::GetMetafileHeader
f1_keywords:
- gdiplusheaders/Metafile::GetMetafileHeader
dev_langs:
- c++
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

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmetaheader/nl-gdiplusmetaheader-metafileheader">MetafileHeader</a> object that receives the copy of the metafile header.

## -returns

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>

<a href="https://docs.microsoft.com/previous-versions/ms535294(v=vs.85)">Metafile::Metafile</a>

<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmetaheader/nl-gdiplusmetaheader-metafileheader">MetafileHeader</a>

<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-metafiles-use">Loading and Displaying Metafiles</a>
