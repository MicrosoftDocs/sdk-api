---
UID: NE:authif._RADIUS_AUTHENTICATION_PROVIDER
title: RADIUS_AUTHENTICATION_PROVIDER (authif.h)
description: The RADIUS_AUTHENTICATION_PROVIDER type enumerates the possible authentication providers that NPS can use.
helpviewer_keywords: ["RADIUS_AUTHENTICATION_PROVIDER","RADIUS_AUTHENTICATION_PROVIDER enumeration [Network Policy Server]","_ias_radius_authentication_provider","authif/RADIUS_AUTHENTICATION_PROVIDER","authif/rapMCIS","authif/rapNone","authif/rapODBC","authif/rapProxy","authif/rapUnknown","authif/rapUsersFile","authif/rapWindowsNT","ias.radius_authentication_provider","nps.IAS_radius_authentication_provider","rapMCIS","rapNone","rapODBC","rapProxy","rapUnknown","rapUsersFile","rapWindowsNT"]
old-location: nps\IAS_radius_authentication_provider.htm
tech.root: Nps
ms.assetid: 017c31f1-1654-4312-a1f0-747ea82391e1
ms.date: 12/05/2018
ms.keywords: RADIUS_AUTHENTICATION_PROVIDER, RADIUS_AUTHENTICATION_PROVIDER enumeration [Network Policy Server], _ias_radius_authentication_provider, authif/RADIUS_AUTHENTICATION_PROVIDER, authif/rapMCIS, authif/rapNone, authif/rapODBC, authif/rapProxy, authif/rapUnknown, authif/rapUsersFile, authif/rapWindowsNT, ias.radius_authentication_provider, nps.IAS_radius_authentication_provider, rapMCIS, rapNone, rapODBC, rapProxy, rapUnknown, rapUsersFile, rapWindowsNT
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
req.typenames: RADIUS_AUTHENTICATION_PROVIDER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RADIUS_AUTHENTICATION_PROVIDER
 - authif/_RADIUS_AUTHENTICATION_PROVIDER
 - RADIUS_AUTHENTICATION_PROVIDER
 - authif/RADIUS_AUTHENTICATION_PROVIDER
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
 - RADIUS_AUTHENTICATION_PROVIDER
---

# RADIUS_AUTHENTICATION_PROVIDER enumeration


## -description

<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The 
<b>RADIUS_AUTHENTICATION_PROVIDER</b> type enumerates the possible authentication providers that NPS can use.

## -enum-fields

### -field rapUnknown

The authentication provider is unknown.

### -field rapUsersFile

A users' file  provides the authentication information.

### -field rapProxy

Authentication is provided by a RADIUS proxy server.

### -field rapWindowsNT

Authentication is provided by Windows Domain Authentication.

### -field rapMCIS

Authentication is provided by a Microsoft Commercial Internet System (MCIS) database.

### -field rapODBC

Authentication is provided by an Open Database Connectivity (ODBC) compliant database.

### -field rapNone

Access is unauthenticated.

## -remarks

The <b>ratProvider</b> extended attribute in 
<a href="/windows/desktop/api/authif/ne-authif-radius_attribute_type">RADIUS_ATTRIBUTE_TYPE</a> uses values from the 
<b>RADIUS_AUTHENTICATION_PROVIDER</b> enumeration type.

## -see-also

<a href="/windows/desktop/Nps/ias-about-internet-authentication-service">About NPS Extensions</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-enumerations">NPS Extensions Enumerations</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-reference">NPS Extensions Reference</a>



<a href="/windows/desktop/api/authif/ns-authif-radius_attribute">RADIUS_ATTRIBUTE</a>



<a href="/windows/desktop/api/authif/ne-authif-radius_attribute_type">RADIUS_ATTRIBUTE_TYPE</a>