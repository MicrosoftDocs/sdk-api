---
UID: NF:sbe.IStreamBufferDataCounters.GetData
title: IStreamBufferDataCounters::GetData (sbe.h)
description: The GetData method returns performance data for the Stream Buffer Engine.
helpviewer_keywords: ["GetData","GetData method [Microsoft TV Technologies]","GetData method [Microsoft TV Technologies]","IStreamBufferDataCounters interface","IStreamBufferDataCounters interface [Microsoft TV Technologies]","GetData method","IStreamBufferDataCounters.GetData","IStreamBufferDataCounters::GetData","IStreamBufferDataCountersGetData","mstv.istreambufferdatacounters_getdata","sbe/IStreamBufferDataCounters::GetData"]
old-location: mstv\istreambufferdatacounters_getdata.htm
tech.root: mstv
ms.assetid: 15895ff3-37e5-4f89-bcce-3b9f060c0746
ms.date: 12/05/2018
ms.keywords: GetData, GetData method [Microsoft TV Technologies], GetData method [Microsoft TV Technologies],IStreamBufferDataCounters interface, IStreamBufferDataCounters interface [Microsoft TV Technologies],GetData method, IStreamBufferDataCounters.GetData, IStreamBufferDataCounters::GetData, IStreamBufferDataCountersGetData, mstv.istreambufferdatacounters_getdata, sbe/IStreamBufferDataCounters::GetData
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStreamBufferDataCounters::GetData
 - sbe/IStreamBufferDataCounters::GetData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferDataCounters.GetData
---

# IStreamBufferDataCounters::GetData


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetData</b> method returns performance data for the Stream Buffer Engine.

## -parameters

### -param pPinData [in]

Pointer to an <a href="/previous-versions/windows/desktop/api/sbe/ns-sbe-sbe_pin_data">SBE_PIN_DATA</a> structure. The method fills the structure with the current performance data.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferdatacounters">IStreamBufferDataCounters Interface</a>