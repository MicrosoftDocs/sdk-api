---
UID: NF:raseapif.RasEapGetInfo
title: RasEapGetInfo function (raseapif.h)
description: The RAS connection manager calls RasEapGetInfo to obtain a set of function pointers for a specified authentication protocol.
helpviewer_keywords: ["RasEapGetInfo","RasEapGetInfo callback","RasEapGetInfo callback function [EAP]","_eap_raseapgetinfo","eap.raseapgetinfo","raseapif/RasEapGetInfo"]
old-location: eap\raseapgetinfo.htm
tech.root: EAP
ms.assetid: e75964b9-f5d6-494e-8620-07f0e97bcd09
ms.date: 12/05/2018
ms.keywords: RasEapGetInfo, RasEapGetInfo callback, RasEapGetInfo callback function [EAP], _eap_raseapgetinfo, eap.raseapgetinfo, raseapif/RasEapGetInfo
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasEapGetInfo
 - raseapif/RasEapGetInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Raseapif.h
api_name:
 - RasEapGetInfo
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
<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_info">PPP_EAP_INFO</a> structure. The structure receives members that RAS sets to identify the structure version and the authentication protocol for which function pointers are requested. For more information, see 
<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_info">PPP_EAP_INFO</a>.

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
[EAP Overview](/windows/win32/eap/eap-installation).

If the function returns any value other than <b>NO_ERROR</b>, RAS considers the authentication protocol to be non-functional. RAS posts an error to the  Windows NT/Windows 2000 Event Log to indicate that this protocol did not start correctly and therefore is not available.

## -see-also

[EAP (Extensible Authentication Protocol) Overview](/windows/win32/eap/about-extensible-authentication-protocol)



[EAP Functions](/windows/win32/eap/eap-functions)



[Extensible Authentication Protocol Reference](/windows/win32/eap/extensible-authentication-protocol-reference)



<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_info">PPP_EAP_INFO</a>