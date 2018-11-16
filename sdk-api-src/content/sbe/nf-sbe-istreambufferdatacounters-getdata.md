---
UID: NF:sbe.IStreamBufferDataCounters.GetData
title: IStreamBufferDataCounters::GetData
author: windows-sdk-content
description: The GetData method returns performance data for the Stream Buffer Engine.
old-location: mstv\istreambufferdatacounters_getdata.htm
tech.root: mstv
ms.assetid: 15895ff3-37e5-4f89-bcce-3b9f060c0746
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetData, GetData method [Microsoft TV Technologies], GetData method [Microsoft TV Technologies],IStreamBufferDataCounters interface, IStreamBufferDataCounters interface [Microsoft TV Technologies],GetData method, IStreamBufferDataCounters.GetData, IStreamBufferDataCounters::GetData, IStreamBufferDataCountersGetData, mstv.istreambufferdatacounters_getdata, sbe/IStreamBufferDataCounters::GetData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferDataCounters.GetData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- sbe.h
: 
- IStreamBufferDataCounters.GetData
: 
---

# IStreamBufferDataCounters::GetData


## -description


The <b>GetData</b> method returns performance data for the Stream Buffer Engine.


## -parameters




### -param pPinData [in]

Pointer to an <a href="https://msdn.microsoft.com/727aa921-5156-4b7a-a184-b0744acfa6fb">SBE_PIN_DATA</a> structure. The method fills the structure with the current performance data.


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




<a href="https://msdn.microsoft.com/d9394d04-ba6b-4946-b33a-9c53070238f7">IStreamBufferDataCounters Interface</a>
 

 

