---
UID: NF:gdiplusheaders.Metafile.GetMetafileHeader
title: Metafile::GetMetafileHeader
description: The Metafile::GetMetafileHeader method gets the metafile header of this metafile.
ms.assetid: 5d12078c-4492-4bd1-a68b-8ff06dede784
ms.author: windowssdkdev
ms.date: 05/20/2019
ms.keywords: Metafile::GetMetafileHeader
ms.topic: language-reference
f1_keywords: ["gdiplusheaders/Metafile::GetMetafileHeader"]
targetos: Windows
product: Windows
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

<a href="https://docs.microsoft.com/previous-versions//ms535294(v=vs.85)">Metafile::Metafile</a>

<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmetaheader/nl-gdiplusmetaheader-metafileheader">MetafileHeader</a>

<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-metafiles-use">Loading and Displaying Metafiles</a>
