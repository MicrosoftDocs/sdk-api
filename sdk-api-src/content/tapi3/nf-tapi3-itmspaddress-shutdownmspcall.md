---
UID: NF:tapi3.ITMSPAddress.ShutdownMSPCall
title: ITMSPAddress::ShutdownMSPCall
author: windows-sdk-content
description: The ShutdownMSPCall method is called when the call object is being destroyed.
old-location: tapi3\itmspaddress_shutdownmspcall.htm
tech.root: TAPI
ms.assetid: 6527db85-cad8-4b0d-977a-9ab8b047e44e
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITMSPAddress interface [TAPI 2.2],ShutdownMSPCall method, ITMSPAddress.ShutdownMSPCall, ITMSPAddress::ShutdownMSPCall, ShutdownMSPCall, ShutdownMSPCall method [TAPI 2.2], ShutdownMSPCall method [TAPI 2.2],ITMSPAddress interface, _tapi3_itmspaddress_shutdownmspcall, msp/ITMSPAddress::ShutdownMSPCall, tapi3.itmspaddress_shutdownmspcall
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msp.h
api_name:
 - ITMSPAddress.ShutdownMSPCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITMSPAddress::ShutdownMSPCall


## -description


The 
<b>ShutdownMSPCall</b> method is called when the call object is being destroyed.


## -parameters




### -param pStreamControl [in]

Pointer to <a href="_com_iunknown">IUnknown</a> interface for the call's 
<a href="https://msdn.microsoft.com/12b9457a-7afb-4348-93a2-28728c673929">ITStreamControl</a>.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pStreamControl</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pStreamControl</i> parameter does not point to a valid 
<a href="https://msdn.microsoft.com/12b9457a-7afb-4348-93a2-28728c673929">ITStreamControl</a> interface.

</td>
</tr>
</table>
 




## -remarks



This method is not automatically invoked when a call enters the disconnect state. The paired TSP of the MSP should notify the MSP of this call state change, but, because applications may retain the call object for information logging purposes after a disconnect, shutdown should not be called until the call object itself is released.




## -see-also




<a href="https://msdn.microsoft.com/246a0bcd-0dbb-4b77-a1cd-e6378eaff889">ITMSPAddress</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

