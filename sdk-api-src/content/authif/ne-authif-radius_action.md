---
UID: NE:authif._RADIUS_ACTION
title: RADIUS_ACTION (authif.h)
description: The RADIUS_ACTION type enumerates the responses that a NPS Extension DLL can generate in response to an Access-Request.
helpviewer_keywords: ["*PRADIUS_ACTION","PRADIUS_ACTION","PRADIUS_ACTION enumeration pointer [Network Policy Server]","RADIUS_ACTION","RADIUS_ACTION enumeration [Network Policy Server]","_ias_radius_action","authif/PRADIUS_ACTION","authif/RADIUS_ACTION","authif/raAccept","authif/raContinue","authif/raReject","ias.radius_action","nps.IAS_radius_action","raAccept","raContinue","raReject"]
old-location: nps\IAS_radius_action.htm
tech.root: Nps
ms.assetid: c0bd58ca-24e5-4cee-95e9-521d15c44814
ms.date: 12/05/2018
ms.keywords: '*PRADIUS_ACTION, PRADIUS_ACTION, PRADIUS_ACTION enumeration pointer [Network Policy Server], RADIUS_ACTION, RADIUS_ACTION enumeration [Network Policy Server], _ias_radius_action, authif/PRADIUS_ACTION, authif/RADIUS_ACTION, authif/raAccept, authif/raContinue, authif/raReject, ias.radius_action, nps.IAS_radius_action, raAccept, raContinue, raReject'
req.header: authif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
req.typenames: RADIUS_ACTION, *PRADIUS_ACTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RADIUS_ACTION
 - authif/_RADIUS_ACTION
 - PRADIUS_ACTION
 - authif/PRADIUS_ACTION
 - RADIUS_ACTION
 - authif/RADIUS_ACTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AuthIf.h
api_name:
 - RADIUS_ACTION
---

# RADIUS_ACTION enumeration


## -description

<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The 
<b>RADIUS_ACTION</b> type enumerates the responses that a NPS Extension DLL can generate in response to an Access-Request.

## -enum-fields

### -field raContinue

NPS continues to process the request. NPS also continues to call 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process">RadiusExtensionProcess</a> in other Extension DLLs.

### -field raReject

Return an Access-Reject packet. The Access-Request is declined. In this case, NPS does not call 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process">RadiusExtensionProcess</a> in any other Extension DLLs.

### -field raAccept

NPS accepts the Access-Request. NPS does not continue to call 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process">RadiusExtensionProcess</a> in this case. However, it does continue to obtain authorizations for the user requesting access.

## -remarks

Use the values for this enumeration only as the actions for the 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process">RadiusExtensionProcess</a> and 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex">RadiusExtensionProcessEx</a> functions.

## -see-also

<a href="/windows/desktop/Nps/ias-about-internet-authentication-service">About NPS Extensions</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-enumerations">NPS Extensions Enumerations</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-reference">NPS Extensions Reference</a>



<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process">RadiusExtensionProcess</a>



<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex">RadiusExtensionProcessEx</a>