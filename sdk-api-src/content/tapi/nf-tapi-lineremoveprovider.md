---
UID: NF:tapi.lineRemoveProvider
title: lineRemoveProvider function
author: windows-sdk-content
description: The lineRemoveProvider function removes an existing telephony service provider from the telephony system.
old-location: tapi2\lineremoveprovider.htm
tech.root: tapi
ms.assetid: 8398a869-bc64-490a-bdb2-496582a88d84
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "_tapi2_lineremoveprovider, lineRemoveProvider, lineRemoveProvider function [TAPI 2.2], tapi/lineRemoveProvider, tapi2.lineremoveprovider"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tapi.h
req.include-header: 
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineRemoveProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineRemoveProvider function


## -description


The 
<b>lineRemoveProvider</b> function removes an existing telephony service provider from the telephony system.


## -parameters




### -param dwPermanentProviderID

Permanent provider identifier of the service provider to be removed.


### -param hwndOwner

Handle to a window to which any dialog boxes that need to be displayed as part of the removal process (for example, a confirmation dialog box by the service provider's 
<a href="https://msdn.microsoft.com/3d6c6183-d5ab-4939-8f44-dfc42458706f">TSPI_providerRemove</a> function) would be attached. Can be a <b>NULL</b> value to indicate that any window created during the function should have no owner window.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INIFILECORRUPT, LINEERR_NOMEM, LINEERR_INVALPARAM, LINEERR_OPERATIONFAILED.




## -remarks



If the call to 
<a href="https://msdn.microsoft.com/3d6c6183-d5ab-4939-8f44-dfc42458706f">TSPI_providerRemove</a> succeeds, and the telephony system is active at the time, TAPI calls 
<a href="https://msdn.microsoft.com/d512508a-fb6a-41ec-a80d-f625abfdd184">lineShutdown</a> and/or 
<a href="https://msdn.microsoft.com/0cf8bc07-946a-450d-8062-b9e19c22a4c5">phoneShutdown</a> on the service provider (depending on which device types are active). Any line or phone handles still held by applications on associated devices are forcibly closed with 
<a href="https://msdn.microsoft.com/f254e331-d574-4fa7-8447-6e4535d3d773">LINE_CLOSE</a> or 
<a href="https://msdn.microsoft.com/84650abf-235e-4792-a67d-2f0f08b85a32">PHONE_CLOSE</a> messages (it is preferable for service providers to issue these messages as part of 
<a href="https://msdn.microsoft.com/3d6c6183-d5ab-4939-8f44-dfc42458706f">TSPI_providerRemove</a>, after verification with the user). The devices previously under the control of that provider are then marked as "unavailable", so that any future attempts by applications to reference them by device identifier result in LINEERR_NODRIVER.




## -see-also




<a href="https://msdn.microsoft.com/f254e331-d574-4fa7-8447-6e4535d3d773">LINE_CLOSE</a>



<a href="https://msdn.microsoft.com/84650abf-235e-4792-a67d-2f0f08b85a32">PHONE_CLOSE</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

