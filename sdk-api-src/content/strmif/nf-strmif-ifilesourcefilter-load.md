---
UID: NF:strmif.IFileSourceFilter.Load
title: IFileSourceFilter::Load (strmif.h)
description: The Load method causes a source filter to load a media file.helpviewer_keywords: ["IFileSourceFilter interface [DirectShow]","Load method","IFileSourceFilter.Load","IFileSourceFilter::Load","IFileSourceFilterLoad","Load","Load method [DirectShow]","Load method [DirectShow]","IFileSourceFilter interface","dshow.ifilesourcefilter_load","strmif/IFileSourceFilter::Load"]
old-location: dshow\ifilesourcefilter_load.htm
tech.root: DirectShow
ms.assetid: a44b8153-19d5-43ad-936c-214c694eeeb6
ms.date: 12/05/2018
ms.keywords: IFileSourceFilter interface [DirectShow],Load method, IFileSourceFilter.Load, IFileSourceFilter::Load, IFileSourceFilterLoad, Load, Load method [DirectShow], Load method [DirectShow],IFileSourceFilter interface, dshow.ifilesourcefilter_load, strmif/IFileSourceFilter::Load
f1_keywords:
- strmif/IFileSourceFilter.Load
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IFileSourceFilter.Load
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFileSourceFilter::Load


## -description



The <code>Load</code> method causes a source filter to load a media file.




## -parameters




### -param pszFileName [in]

Pointer to the name of the file to open.


### -param pmt [in]

Pointer to the media type of the file. This can be <b>NULL</b>.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method initializates the interface. It is not designed to load multiple files, and any calls to this method after the first call will fail.

For the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/file-source--async--filter">File Source (Async)</a> filter, <i>pszFileName</i> specifies the absolute path name of a local file. For the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/file-source--url--filter">File Source (URL)</a> filter, <i>pszFileName</i> specifies the URL of a file to download. For other filter implementations, <i>pszFileName</i> might require a file name or a URL, depending on the filter.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifilesourcefilter">IFileSourceFilter Interface</a>
 

 

