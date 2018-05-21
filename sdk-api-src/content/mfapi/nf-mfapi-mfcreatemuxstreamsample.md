---
UID: NF:mfapi.MFCreateMuxStreamSample
title: MFCreateMuxStreamSample function
author: windows-driver-content
description: Creates an IMFSample containing the samples of multiplexed substreams.
old-location: mf\mfcreatemuxstreamsample.htm
old-project: medfound
ms.assetid: D7E7B260-54E0-47F4-9762-ADB06103CDF3
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: MFCreateMuxStreamSample, MFCreateMuxStreamSample function [Media Foundation], mf.mfcreatemuxstreamsample, mfapi/MFCreateMuxStreamSample
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mfplat.dll
api_name:
-	MFCreateMuxStreamSample
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateMuxStreamSample function


## -description


Creates an <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> containing the samples of multiplexed substreams.


## -parameters




### -param pSamplesToMux [in]

The collection containing the  <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> for each multiplexed substream.


### -param ppMuxSample [out]

The <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> containing the samples for the multiplexed substreams.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pSamplesToMux</i> parameter in null.

</td>
</tr>
</table>
 



