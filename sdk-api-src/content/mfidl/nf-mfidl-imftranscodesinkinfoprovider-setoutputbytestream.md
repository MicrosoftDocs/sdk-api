---
UID: NF:mfidl.IMFTranscodeSinkInfoProvider.SetOutputByteStream
title: IMFTranscodeSinkInfoProvider::SetOutputByteStream method
author: windows-driver-content
description: Sets an output byte stream for the transcode media sink.
old-location: mf\imftranscodesinkinfoprovider_setoutputbytestream.htm
old-project: medfound
ms.assetid: 234bed82-a148-4313-a8cb-eefe2061b7ed
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: IMFTranscodeSinkInfoProvider, IMFTranscodeSinkInfoProvider interface [Media Foundation], SetOutputByteStream method, IMFTranscodeSinkInfoProvider::SetOutputByteStream, SetOutputByteStream method [Media Foundation], SetOutputByteStream method [Media Foundation], IMFTranscodeSinkInfoProvider interface, SetOutputByteStream,IMFTranscodeSinkInfoProvider.SetOutputByteStream, mf.imftranscodesinkinfoprovider_setoutputbytestream, mfidl/IMFTranscodeSinkInfoProvider::SetOutputByteStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfidl.h
api_name:
-	IMFTranscodeSinkInfoProvider.SetOutputByteStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTranscodeSinkInfoProvider::SetOutputByteStream method


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
 

 

