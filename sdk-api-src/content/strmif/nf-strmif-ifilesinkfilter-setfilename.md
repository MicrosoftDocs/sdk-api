---
UID: NF:strmif.IFileSinkFilter.SetFileName
title: IFileSinkFilter::SetFileName
author: windows-sdk-content
description: The SetFileName method sets the name of the file into which media samples will be written.
old-location: dshow\ifilesinkfilter_setfilename.htm
old-project: DirectShow
ms.assetid: d202be46-0a7a-4097-adf6-6ec9c6274449
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IFileSinkFilter interface [DirectShow],SetFileName method, IFileSinkFilter.SetFileName, IFileSinkFilter2 interface [DirectShow],SetFileName method, IFileSinkFilter2::SetFileName, IFileSinkFilter::SetFileName, IFileSinkFilterSetFileName, SetFileName, SetFileName method [DirectShow], SetFileName method [DirectShow],IFileSinkFilter interface, SetFileName method [DirectShow],IFileSinkFilter2 interface, dshow.ifilesinkfilter_setfilename, strmif/IFileSinkFilter2::SetFileName, strmif/IFileSinkFilter::SetFileName
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
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
-	IFileSinkFilter.SetFileName
-	IFileSinkFilter2.SetFileName
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IFileSinkFilter::SetFileName


## -description



The <code>SetFileName</code> method sets the name of the file into which media samples will be written.




## -parameters




### -param pszFileName [in]

Pointer to the name of the file to receive the media samples.


### -param pmt [in]

Pointer to the type of media samples to be written to the file, and the media type of the sink filter's input pin.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



If the <i>pszFileName</i> parameter names a nonexistent file, the file will be created. If it names an existing file, the sink filter will overwrite the file without first deleting it.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/aa1d3f8e-9790-4442-ba7e-896981bf1b96">IFileSinkFilter Interface</a>



<a href="https://msdn.microsoft.com/1339c441-2b10-461f-87f3-4835c1692740">IFileSinkFilter2</a>
 

 

