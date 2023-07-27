---
UID: NF:strmif.IFilterMapper2.CreateCategory
title: IFilterMapper2::CreateCategory (strmif.h)
description: The CreateCategory method adds a new filter category to the registry.
helpviewer_keywords: ["CreateCategory","CreateCategory method [DirectShow]","CreateCategory method [DirectShow]","IFilterMapper2 interface","IFilterMapper2 interface [DirectShow]","CreateCategory method","IFilterMapper2.CreateCategory","IFilterMapper2::CreateCategory","IFilterMapper2CreateCategory","dshow.ifiltermapper2_createcategory","strmif/IFilterMapper2::CreateCategory"]
old-location: dshow\ifiltermapper2_createcategory.htm
tech.root: dshow
ms.assetid: 37dc50a0-530c-4b31-b766-9e161b04c6d5
ms.date: 4/26/2023
ms.keywords: CreateCategory, CreateCategory method [DirectShow], CreateCategory method [DirectShow],IFilterMapper2 interface, IFilterMapper2 interface [DirectShow],CreateCategory method, IFilterMapper2.CreateCategory, IFilterMapper2::CreateCategory, IFilterMapper2CreateCategory, dshow.ifiltermapper2_createcategory, strmif/IFilterMapper2::CreateCategory
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFilterMapper2::CreateCategory
 - strmif/IFilterMapper2::CreateCategory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFilterMapper2.CreateCategory
---

# IFilterMapper2::CreateCategory


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>CreateCategory</code> method adds a new filter category to the registry.

## -parameters

### -param clsidCategory [in]

Class identifier (CLSID) of the new filter category.

### -param dwCategoryMerit [in]

<a href="/windows/desktop/DirectShow/merit">Merit</a> of the category. Categories with higher merit are enumerated first.

### -param Description [in]

Descriptive name for the category.

## -returns

Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.

## -remarks

The filter graph manager initially skips all categories with a merit value less than or equal to MERIT_DO_NOT_USE, to speed up the graph-building process. Filter categories that should not be considered for playback should have a merit of MERIT_DO_NOT_USE or less.

A filter can appear in one or more categories (for example, Video Compressors) to restrict the search space.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifiltermapper2">IFilterMapper2 Interface</a>