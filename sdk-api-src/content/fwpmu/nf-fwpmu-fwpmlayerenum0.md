---
UID: NF:fwpmu.FwpmLayerEnum0
title: FwpmLayerEnum0 function
author: windows-driver-content
description: Returns the next page of results from the layer enumerator.
old-location: fwp\fwpmlayerenum0_func.htm
old-project: FWP
ms.assetid: 0bcf0b85-713f-4f82-9cb5-cb1725c8167b
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: FwpmLayerEnum0, FwpmLayerEnum0 function [Filtering], fwp.fwpmlayerenum0_func, fwpmu/FwpmLayerEnum0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Fwpuclnt.dll
api_name:
-	FwpmLayerEnum0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmLayerEnum0 function


## -description


The <b>FwpmLayerEnum0</b> function returns the next page of results from the layer enumerator.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param enumHandle [in]

Type: <b>HANDLE</b>

Handle for a layer enumeration created by a call to <a href="https://msdn.microsoft.com/94738168-9f02-420a-96cd-b7c3f6418c6f">FwpmLayerCreateEnumHandle0</a>.


### -param numEntriesRequested [in]

Type: <b>UINT32</b>

The number of layer entries requested.


### -param entries [out]

Type: <b><a href="https://msdn.microsoft.com/77d567a7-9495-4f16-9b02-e44a1ef67022">FWPM_LAYER0</a>***</b>

Addresses of the enumeration entries.


### -param numEntriesReturned [out]

Type: <b>UINT32*</b>

The number of layer entries returned.


## -returns



Type: <b>DWORD</b>

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The layers were enumerated successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_* error code</b></dt>
<dt>0x80320001—0x80320039</dt>
</dl>
</td>
<td width="60%">
A Windows Filtering Platform (WFP) specific error. See <a href="https://msdn.microsoft.com/11f3085a-f044-4a78-b47a-59b9086562bf">WFP Error Codes</a> for details.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_* error code</b></dt>
<dt>0x80010001—0x80010122</dt>
</dl>
</td>
<td width="60%">
Failure to communicate with the remote or local firewall engine.

</td>
</tr>
</table>
 




## -remarks



If the <i>numEntriesReturned</i> is less than the <i>numEntriesRequested</i>, the enumeration is exhausted. 

The returned array of entries (but not the individual entries themselves) must be freed by a call to <a href="https://msdn.microsoft.com/ba9f8c1e-f75c-4bf0-b68b-e21a358575fc">FwpmFreeMemory0</a>.

A subsequent call using the same enumeration handle will return the next set of items following those in the last output buffer.

<b>FwpmLayerEnum0</b> is a specific implementation of FwpmLayerEnum. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/77d567a7-9495-4f16-9b02-e44a1ef67022">FWPM_LAYER0</a>



<a href="https://msdn.microsoft.com/94738168-9f02-420a-96cd-b7c3f6418c6f">FwpmLayerCreateEnumHandle0</a>
 

 

