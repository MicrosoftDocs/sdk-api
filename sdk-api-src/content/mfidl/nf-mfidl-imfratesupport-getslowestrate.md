---
UID: NF:mfidl.IMFRateSupport.GetSlowestRate
title: IMFRateSupport::GetSlowestRate
author: windows-sdk-content
description: Retrieves the slowest playback rate supported by the object.
old-location: mf\imfratesupport_getslowestrate.htm
tech.root: medfound
ms.assetid: e10125e9-8bc7-4fb6-8a10-ba5717f1596f
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetSlowestRate, GetSlowestRate method [Media Foundation], GetSlowestRate method [Media Foundation],IMFRateSupport interface, IMFRateSupport interface [Media Foundation],GetSlowestRate method, IMFRateSupport.GetSlowestRate, IMFRateSupport::GetSlowestRate, e10125e9-8bc7-4fb6-8a10-ba5717f1596f, mf.imfratesupport_getslowestrate, mfidl/IMFRateSupport::GetSlowestRate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFRateSupport.GetSlowestRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFRateSupport::GetSlowestRate


## -description



Retrieves the slowest playback rate supported by the object.




## -parameters




### -param eDirection [in]

Specifies whether to query to the slowest forward playback rate or reverse playback rate. The value is a member of the <a href="https://msdn.microsoft.com/34cc861c-ab15-48f4-bb6e-736b70383546">MFRATE_DIRECTION</a> enumeration.


### -param fThin [in]

If <b>TRUE</b>, the method retrieves the slowest thinned playback rate. Otherwise, the method retrieves the slowest non-thinned playback rate. For information about thinning, see <a href="https://msdn.microsoft.com/509b2cc8-6017-41a9-ae80-9af21dce9367">About Rate Control</a>.


### -param pflRate [out]

Receives the slowest playback rate that the object supports.


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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_REVERSE_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The object does not support reverse playback.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_THINNING_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The object does not support thinning.

</td>
</tr>
</table>
 




## -remarks



The value returned in <i>plfRate</i> represents a lower bound. Playback at this rate is not guaranteed. Call <a href="https://msdn.microsoft.com/3ac04683-17d3-4d87-b260-39b04eab9e59">IMFRateSupport::IsRateSupported</a> to check whether the boundary rate is supported. For example, a component that supports arbitrarily slow rates will return zero in <i>pflRate</i>, and applications should call <b>IsRateSupported</b> separately to determine whether the component supports rate 0.

If <i>eDirection</i> is MFRATE_REVERSE, the method retrieves the slowest reverse playback rate. This is a negative value, assuming the object supports reverse playback.




## -see-also




<a href="https://msdn.microsoft.com/7f2b64e1-1062-4f77-b8e0-62b6d962ae8b">How to Determine Supported Rates</a>



<a href="https://msdn.microsoft.com/a6c495fa-0f6a-4e4c-8fba-996b22d55053">IMFRateSupport</a>
 

 

