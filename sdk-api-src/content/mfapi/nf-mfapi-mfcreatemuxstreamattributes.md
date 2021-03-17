---
UID: NF:mfapi.MFCreateMuxStreamAttributes
title: MFCreateMuxStreamAttributes function (mfapi.h)
description: Creates an IMFAttributes describing the content of multiplexed substreams.
helpviewer_keywords: ["MFCreateMuxStreamAttributes","MFCreateMuxStreamAttributes function [Media Foundation]","mf.mfcreatemuxstreamattributes","mfapi/MFCreateMuxStreamAttributes"]
old-location: mf\mfcreatemuxstreamattributes.htm
tech.root: mf
ms.assetid: 946D56BC-13A2-4464-8399-22A74E26693E
ms.date: 12/05/2018
ms.keywords: MFCreateMuxStreamAttributes, MFCreateMuxStreamAttributes function [Media Foundation], mf.mfcreatemuxstreamattributes, mfapi/MFCreateMuxStreamAttributes
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateMuxStreamAttributes
 - mfapi/MFCreateMuxStreamAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateMuxStreamAttributes
---

# MFCreateMuxStreamAttributes function


## -description

Creates an <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> describing the content of multiplexed substreams.

## -parameters

### -param pAttributesToMux [in]

The collection containing the  <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> for each multiplexed substream.

### -param ppMuxAttribs [out]

The <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> containing the attributes for the multiplexed substreams.

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
The <i>pAttributesToMux</i> parameter in null.

</td>
</tr>
</table>