---
UID: NF:strmif.IFileSinkFilter.SetFileName
title: IFileSinkFilter::SetFileName (strmif.h)
author: windows-sdk-content
description: The SetFileName method sets the name of the file into which media samples will be written.
old-location: dshow\ifilesinkfilter_setfilename.htm
tech.root: DirectShow
ms.assetid: d202be46-0a7a-4097-adf6-6ec9c6274449
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFileSinkFilter interface [DirectShow],SetFileName method, IFileSinkFilter.SetFileName, IFileSinkFilter2 interface [DirectShow],SetFileName method, IFileSinkFilter2::SetFileName, IFileSinkFilter::SetFileName, IFileSinkFilterSetFileName, SetFileName, SetFileName method [DirectShow], SetFileName method [DirectShow],IFileSinkFilter interface, SetFileName method [DirectShow],IFileSinkFilter2 interface, dshow.ifilesinkfilter_setfilename, strmif/IFileSinkFilter2::SetFileName, strmif/IFileSinkFilter::SetFileName
ms.topic: method
f1_keywords: 
 - "strmif/IFileSinkFilter.SetFileName"
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
 - IFileSinkFilter.SetFileName
 - IFileSinkFilter2.SetFileName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifilesinkfilter">IFileSinkFilter Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ifilesinkfilter2">IFileSinkFilter2</a>
 

 

