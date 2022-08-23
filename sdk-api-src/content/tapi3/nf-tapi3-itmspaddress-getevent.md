---
UID: NF:tapi3.ITMSPAddress.GetEvent
title: ITMSPAddress::GetEvent (tapi3.h)
description: The ITMSPAddress::GetEvent (tapi3.h) method retrieves event information.
helpviewer_keywords: ["GetEvent","GetEvent method [TAPI 2.2]","GetEvent method [TAPI 2.2]","ITMSPAddress interface","ITMSPAddress interface [TAPI 2.2]","GetEvent method","ITMSPAddress.GetEvent","ITMSPAddress::GetEvent","_tapi3_itmspaddress_getevent","msp/ITMSPAddress::GetEvent","tapi3.itmspaddress_getevent"]
old-location: tapi3\itmspaddress_getevent.htm
tech.root: tapi3
ms.assetid: df5263f2-9d76-472d-b7fc-724d36f0b58f
ms.date: 08/09/2022
ms.keywords: GetEvent, GetEvent method [TAPI 2.2], GetEvent method [TAPI 2.2],ITMSPAddress interface, ITMSPAddress interface [TAPI 2.2],GetEvent method, ITMSPAddress.GetEvent, ITMSPAddress::GetEvent, _tapi3_itmspaddress_getevent, msp/ITMSPAddress::GetEvent, tapi3.itmspaddress_getevent
req.header: tapi3.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITMSPAddress::GetEvent
 - tapi3/ITMSPAddress::GetEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msp.h
api_name:
 - ITMSPAddress.GetEvent
---

# ITMSPAddress::GetEvent


## -description

The 
<b>GetEvent</b> method retrieves event information.

## -parameters

### -param pdwSize [in, out]

A pointer to a DWORD that contains the size, in bytes, of <i>pEventBuffer</i>.   On success, <i>pdwSize</i> returns the actual number of bytes in  <i>pEventBuffer</i>. If <i>pEventBuffer</i> is not large enough, the method returns <b>TAPI_E_NOTENOUGHMEMORY</b> and 
    this parameter returns the number, in bytes, required.

### -param pEventBuffer

[in, out, size_is(*<i>pdwSize</i>)] A pointer to buffer that contains 
<a href="/windows/win32/api/msp/ns-msp-msp_event_info">MSP event_info</a> information.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwSize</i> or <i>pEventBuffer</i> parameter is not a valid pointer.

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
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NOTENOUGHMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwSize</i> parameter was not large enough for the buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NOEVENT</b></dt>
</dl>
</td>
<td width="60%">
No event has occurred.

</td>
</tr>
</table>

## -remarks

TAPI3 calls this method when the event handle given in initialize is signaled. TAPI will call this method repeatedly until it fails so it can get multiple events. Each call should return only one event structure.

Users of the MSP base classes: This method locks the event list.

## -see-also

<a href="/windows/desktop/api/msp/nn-msp-itmspaddress">ITMSPAddress</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
