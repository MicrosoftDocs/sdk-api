---
UID: NF:tuner.IESIsdbCasResponseEvent.GetStatus
title: IESIsdbCasResponseEvent::GetStatus
author: windows-driver-content
description: Gets the response status returned in an IsdbCasResponse event.
old-location: mstv\iesisdbcasresponseevent_getstatus.htm
old-project: mstv
ms.assetid: 63cf3d47-5aac-4bce-8562-f67df47f83b2
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetStatus, GetStatus method [DirectShow], GetStatus method [DirectShow],IESIsdbCasResponseEvent interface, IESIsdbCasResponseEvent interface [DirectShow],GetStatus method, IESIsdbCasResponseEvent.GetStatus, IESIsdbCasResponseEvent::GetStatus, mstv.iesisdbcasresponseevent_getstatus, tuner/IESIsdbCasResponseEvent::GetStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IESIsdbCasResponseEvent.GetStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IESIsdbCasResponseEvent::GetStatus


## -description


Gets the response status returned in an <a href="https://msdn.microsoft.com/141c6798-5dca-495e-bdbe-f07e457a3d8a">IsdbCasResponse</a> event.


## -parameters




### -param pStatus [out, retval]

Receives the status code. This can have any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x9000</dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x6400</dt>
</dl>
</td>
<td width="60%">
Memory error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x6581</dt>
</dl>
</td>
<td width="60%">
Write error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x6700</dt>
</dl>
</td>
<td width="60%">
Interconnect command length.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x6800</dt>
</dl>
</td>
<td width="60%">
Unsupported class.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x6A86</dt>
</dl>
</td>
<td width="60%">
Incorrect parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x6D00</dt>
</dl>
</td>
<td width="60%">
Unsupported instruction.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x6E00</dt>
</dl>
</td>
<td width="60%">
Unsupported class.

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/141c6798-5dca-495e-bdbe-f07e457a3d8a">IESIsdbCasResponseEvent</a>
 

 

