---
UID: NF:mfidl.MFCreateMuxSink
title: MFCreateMuxSink function
author: windows-sdk-content
description: Creates a generic media sink that wraps a multiplexer Microsoft Media Foundation transform (MFT).
old-location: mf\mfcreatemuxsink.htm
tech.root: medfound
ms.assetid: 31A8790B-4C71-4D0D-B686-27B345745872
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: MFCreateMuxSink, MFCreateMuxSink function [Media Foundation], mf.mfcreatemuxsink, mfidl/MFCreateMuxSink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateMuxSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateMuxSink function


## -description


Creates a generic media sink that wraps a multiplexer Microsoft Media Foundation transform (MFT).


## -parameters




### -param guidOutputSubType [in]

The subtype GUID of the output type for the MFT.


### -param pOutputAttributes [in]

A list of format attributes for the MFT output type. This parameter is optional and can be <b>NULL</b>.


### -param pOutputByteStream [in]

A pointer to the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface of a byte stream. The output from the MFT is written to this byte stream. This parameter can be <b>NULL</b>.


### -param ppMuxSink [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a> interface of the media sink. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function attempts to find a multiplexer MFT that supports an output type with the following definition:

<ul>
<li>Major type: <b>MFMediaType_Stream</b></li>
<li>Subtype: <i>guidOutputSubType</i></li>
<li>Additional format attributes (optional)</li>
</ul>
To provide a list of additional format attributes:

<ol>
<li>Call <a href="https://msdn.microsoft.com/a79b1edd-5ca1-4550-a6ce-58073155affd">MFCreateAttributes</a> to get an <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> pointer.</li>
<li>Use the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface to set the attributes. (See <a href="https://msdn.microsoft.com/e84ba3f6-4857-4340-baca-5847650ea7b8">Media Type Attributes</a>.)</li>
<li>Pass the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> pointer in the <i>pOutputAttributes</i> parameter.</li>
</ol>
The multiplexer MFT must be registered in the <a href="https://msdn.microsoft.com/eca3ae3b-e40a-407d-986c-d0a85b891f52">MFT_CATEGORY_MULTIPLEXER</a>  category.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

