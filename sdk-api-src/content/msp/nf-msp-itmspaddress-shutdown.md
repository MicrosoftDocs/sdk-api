---
UID: NF:msp.ITMSPAddress.Shutdown
title: ITMSPAddress::Shutdown
author: windows-sdk-content
description: The Shutdown method is called when the MSP is unloaded. Shutdown will be called once per address object.
old-location: tapi3\itmspaddress_shutdown.htm
tech.root: tapi
ms.assetid: 877691cb-b12b-4389-b93c-4ff13a52f4d7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITMSPAddress interface [TAPI 2.2],Shutdown method, ITMSPAddress.Shutdown, ITMSPAddress::Shutdown, Shutdown, Shutdown method [TAPI 2.2], Shutdown method [TAPI 2.2],ITMSPAddress interface, _tapi3_itmspaddress_shutdown, msp/ITMSPAddress::Shutdown, tapi3.itmspaddress_shutdown
ms.topic: method
req.header: msp.h
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
 - ITMSPAddress.Shutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITMSPAddress::Shutdown


## -description


The 
<b>Shutdown</b> method is called when the MSP is unloaded. 
<b>Shutdown</b> will be called once per address object.


## -parameters






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
</table>
 




## -remarks



This method releases the terminals and releases the Terminal Manager. It releases all unprocessed events, and calls 
<a href="https://msdn.microsoft.com/4c108838-ad31-407a-b9af-bfc8c1c4a577">Stop</a> on the global MSP thread object. When this function is called, no call should be alive. However, bugs in the application may keep calls or terminals around.




## -see-also




<a href="https://msdn.microsoft.com/246a0bcd-0dbb-4b77-a1cd-e6378eaff889">ITMSPAddress</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

