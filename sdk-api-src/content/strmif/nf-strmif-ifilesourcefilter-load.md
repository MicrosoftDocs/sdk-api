---
UID: NF:strmif.IFileSourceFilter.Load
title: IFileSourceFilter::Load method
author: windows-driver-content
description: The Load method causes a source filter to load a media file.
old-location: dshow\ifilesourcefilter_load.htm
old-project: DirectShow
ms.assetid: a44b8153-19d5-43ad-936c-214c694eeeb6
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IFileSourceFilter, IFileSourceFilter interface [DirectShow], Load method, IFileSourceFilter::Load, IFileSourceFilterLoad, Load method [DirectShow], Load method [DirectShow], IFileSourceFilter interface, Load,IFileSourceFilter.Load, dshow.ifilesourcefilter_load, strmif/IFileSourceFilter::Load
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IFileSourceFilter.Load
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IFileSourceFilter::Load method


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

For the <a href="https://msdn.microsoft.com/0cf6e7ab-b1fe-42f9-b682-c5484ef48c71">File Source (Async)</a> filter, <i>pszFileName</i> specifies the absolute path name of a local file. For the <a href="https://msdn.microsoft.com/405fd6ea-aa17-4d11-8f07-067468cb090b">File Source (URL)</a> filter, <i>pszFileName</i> specifies the URL of a file to download. For other filter implementations, <i>pszFileName</i> might require a file name or a URL, depending on the filter.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ad70fddb-4fc9-4010-a469-9a8ca4b47379">IFileSourceFilter Interface</a>
 

 

