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

# IMFTranscodeSinkInfoProvider::SetOutputByteStream


## -description


Sets an output byte stream for the transcode media sink.


## -parameters




### -param pByteStreamActivate [in]

A pointer to the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface of a byte-stream activation object. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call this method to provide a writeable byte stream 
        that will receive the transcoded data.

Alternatively, you can provide the name of an  output file, by calling <a href="https://msdn.microsoft.com/048d1822-9349-4d49-a468-c89bc9c51583">IMFTranscodeSinkInfoProvider::SetOutputFile</a>. These two methods are mutually exclusive.

The <i>pByteStreamActivate</i> parameter must specify an activation object that creates a writeable byte stream. Internally, the transcode media sink calls <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">IMFActivate::ActivateObject</a> to create the byte stream, as follows:

<pre class="syntax" xml:space="preserve"><code>IMFByteStream *pByteStream = NULL;

HRESULT hr = pByteStreamActivate-&gt;ActivateObject(IID_IMFByteStream, (void**)&amp;pByteStream);</code></pre>
Currently, Microsoft Media Foundation does not provide any byte-stream activation objects. To use this method, an application must provide a custom implementation of <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a>.




## -see-also




<a href="https://msdn.microsoft.com/c5eb0c30-559a-44dd-80d4-4b11933dc7ce">IMFTranscodeSinkInfoProvider</a>
 

 

