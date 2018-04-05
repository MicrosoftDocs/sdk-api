---
UID: NF:mfapi.MFCreateMuxStreamMediaType
title: MFCreateMuxStreamMediaType function
author: windows-driver-content
description: Creates an IMFMediaType describing the media types of multiplexed substreams.
old-location: mf\mfcreatemuxstreammediatype.htm
old-project: medfound
ms.assetid: 27E1295C-BFB1-45EB-ABB2-DDFF927F6E30
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: MFCreateMuxStreamMediaType, MFCreateMuxStreamMediaType function [Media Foundation], mf.mfcreatemuxstreammediatype, mfapi/MFCreateMuxStreamMediaType
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
-	MFCreateMuxStreamMediaType
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateMuxStreamMediaType function


## -description


Creates an <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> describing the media types  of multiplexed substreams.


## -parameters




### -param pMediaTypesToMux [in]

The collection containing the  <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> for each multiplexed substream.


### -param ppMuxMediaType [out]

The <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> containing the media types for the multiplexed substreams.


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
The <i>pMediaTypesToMux</i> parameter in null.

</td>
</tr>
</table>
 



