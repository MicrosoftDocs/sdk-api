---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

For the <a href="https://msdn.microsoft.com/0cf6e7ab-b1fe-42f9-b682-c5484ef48c71">File Source (Async)</a> filter, <i>pszFileName</i> specifies the absolute path name of a local file. For the <a href="https://msdn.microsoft.com/405fd6ea-aa17-4d11-8f07-067468cb090b">File Source (URL)</a> filter, <i>pszFileName</i> specifies the URL of a file to download. For other filter implementations, <i>pszFileName</i> might require a file name or a URL, depending on the filter.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ad70fddb-4fc9-4010-a469-9a8ca4b47379">IFileSourceFilter Interface</a>
 

 

