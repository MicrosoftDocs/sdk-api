---
UID: NF:raseapif.RasEapGetInfo
title: RasEapGetInfo function
author: windows-sdk-content
description: The RAS connection manager calls RasEapGetInfo to obtain a set of function pointers for a specified authentication protocol.
old-location: eap\raseapgetinfo.htm
old-project: EAP
ms.assetid: e75964b9-f5d6-494e-8620-07f0e97bcd09
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: RasEapGetInfo, RasEapGetInfo callback, RasEapGetInfo callback function [EAP], _eap_raseapgetinfo, eap.raseapgetinfo, raseapif/RasEapGetInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: raseapif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RAS_AUTH_ATTRIBUTE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Raseapif.h
api_name:
 - RasEapGetInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RasEapGetInfo function


## -description


The RAS connection manager calls 
<b>RasEapGetInfo</b> to obtain a set of function pointers for a specified authentication protocol.


## -parameters




### -param dwEapTypeId [in]

Specifies the authentication protocol for which to obtain information.


### -param pEapInfo [out]

Pointer to a 
<a href="https://msdn.microsoft.com/722e8185-3408-418b-ae80-e2ed261edcd1">PPP_EAP_INFO</a> structure. The structure receives members that RAS sets to identify the structure version and the authentication protocol for which function pointers are requested. For more information, see 
<a href="https://msdn.microsoft.com/722e8185-3408-418b-ae80-e2ed261edcd1">PPP_EAP_INFO</a>.


## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value should be an appropriate error code from Winerror.h, Raserror.h, or Mprerror.h.




## -remarks



The DLL that implements 
<b>RasEapGetInfo</b> may support more than one authentication protocol. The <i>dwEapTypeId</i> parameter specifies for which authentication protocol to obtain information.

Implementations of EAP must export the 
<b>RasEapGetInfo</b> function, since RAS uses 
<b>RasEapGetInfo</b> to obtain pointers to the other authentication protocol functions.

Upon initialization, the Connection Manager calls 
<b>RasEapGetInfo</b> for each EAP DLL installed in the registry subkey, as explained in the 
<a href="https://msdn.microsoft.com/af10b1e9-45c9-4640-ba79-fc9c23cc3c47">EAP Overview</a>.

If the function returns any value other than <b>NO_ERROR</b>, RAS considers the authentication protocol to be non-functional. RAS posts an error to the  Windows NT/Windows 2000 Event Log to indicate that this protocol did not start correctly and therefore is not available.




## -see-also




<a href="https://msdn.microsoft.com/a2f41808-4316-431a-ab58-f1e25d3c61f6">EAP (Extensible Authentication Protocol) Overview</a>



<a href="https://msdn.microsoft.com/090a3620-3732-4466-95ac-ce9cbdd36484">EAP Functions</a>



<a href="https://msdn.microsoft.com/d3cb25ce-6fb9-4fca-8662-3efef14238a5">Extensible Authentication Protocol Reference</a>



<a href="https://msdn.microsoft.com/722e8185-3408-418b-ae80-e2ed261edcd1">PPP_EAP_INFO</a>
 

 

