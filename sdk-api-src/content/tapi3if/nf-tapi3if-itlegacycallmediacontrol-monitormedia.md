---
UID: NF:tapi3if.ITLegacyCallMediaControl.MonitorMedia
title: ITLegacyCallMediaControl::MonitorMedia
author: windows-driver-content
description: The MonitorMedia method sets monitoring for a given media type on the current call.
old-location: tapi3\itlegacycallmediacontrol_monitormedia.htm
old-project: Tapi
ms.assetid: 82efd729-fbbf-449f-a347-24bceada140c
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: ITLegacyCallMediaControl interface [TAPI 2.2],MonitorMedia method, ITLegacyCallMediaControl.MonitorMedia, ITLegacyCallMediaControl::MonitorMedia, MonitorMedia, MonitorMedia method [TAPI 2.2], MonitorMedia method [TAPI 2.2],ITLegacyCallMediaControl interface, _tapi3_itlegacycallmediacontrol_monitormedia, tapi3.itlegacycallmediacontrol_monitormedia, tapi3if/ITLegacyCallMediaControl::MonitorMedia
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITLegacyCallMediaControl.MonitorMedia
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITLegacyCallMediaControl::MonitorMedia


## -description


The 
<b>MonitorMedia</b> method sets monitoring for a given media type on the current call. This method enables and disables the detection of media types (modes) on the specified call. When a media type is detected, a message is sent to the application. For more information, see 
<a href="https://msdn.microsoft.com/d79a5469-2248-466b-a5ca-32a568b135d2">lineMonitorMedia</a>.


## -parameters




### -param lMediaType [in]

Indicator of 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a>.


## -returns



This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>lMediaType</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The associated call object is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5f3d0189-fc9d-4fa5-bc8e-a0abf1f607f8">ITLegacyAddressMediaControl</a>



<a href="https://msdn.microsoft.com/73288c46-6c6d-4938-9bb7-4d94acfc67f6">ITLegacyCallMediaControl</a>
 

 

