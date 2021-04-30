---
UID: NE:authif._RADIUS_EXTENSION_POINT
title: RADIUS_EXTENSION_POINT (authif.h)
description: The RADIUS_EXTENSION_POINT enumeration type enumerates the possible points in the RADIUS request process when the RadiusExtensionProcess2 function can be called.
helpviewer_keywords: ["RADIUS_EXTENSION_POINT","RADIUS_EXTENSION_POINT enumeration [Network Policy Server]","_ias_radius_extension_point","authif/RADIUS_EXTENSION_POINT","authif/repAuthentication","authif/repAuthorization","ias.radius_extension_point","nps.IAS_radius_extension_point","repAuthentication","repAuthorization"]
old-location: nps\IAS_radius_extension_point.htm
tech.root: Nps
ms.assetid: 0e7f4d48-01b5-45a8-bf72-27b557ae8da7
ms.date: 12/05/2018
ms.keywords: RADIUS_EXTENSION_POINT, RADIUS_EXTENSION_POINT enumeration [Network Policy Server], _ias_radius_extension_point, authif/RADIUS_EXTENSION_POINT, authif/repAuthentication, authif/repAuthorization, ias.radius_extension_point, nps.IAS_radius_extension_point, repAuthentication, repAuthorization
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
req.typenames: RADIUS_EXTENSION_POINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RADIUS_EXTENSION_POINT
 - authif/_RADIUS_EXTENSION_POINT
 - RADIUS_EXTENSION_POINT
 - authif/RADIUS_EXTENSION_POINT
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
 - RADIUS_EXTENSION_POINT
---

# RADIUS_EXTENSION_POINT enumeration


## -description

<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS.</div><div> </div>The 
<b>RADIUS_EXTENSION_POINT</b> enumeration type enumerates the possible points in the RADIUS request process when the 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process_2">RadiusExtensionProcess2</a> function can be called.

## -enum-fields

### -field repAuthentication

Indicates that the 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process_2">RadiusExtensionProcess2</a> function is called at the point in the request process where authentication occurs.

### -field repAuthorization

Indicates that the 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process_2">RadiusExtensionProcess2</a> function is called at the point in the request process where authorization occurs.

## -remarks

The <b>repPoint</b> member of the 
<a href="/windows/desktop/api/authif/ns-authif-radius_extension_control_block">RADIUS_EXTENSION_CONTROL_BLOCK</a> structure is of type 
<b>RADIUS_EXTENSION_POINT</b>.

See 
<a href="/windows/desktop/Nps/ias-about-internet-authentication-service">About NPS Extensions</a> for a diagram that shows the request process.

## -see-also

<a href="/windows/desktop/Nps/ias-about-internet-authentication-service">About NPS Extensions</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-enumerations">NPS Extensions Enumerations</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-reference">NPS Extensions Reference</a>



<a href="/windows/desktop/api/authif/ns-authif-radius_extension_control_block">RADIUS_EXTENSION_CONTROL_BLOCK</a>



<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process_2">RadiusExtensionProcess2</a>