---
UID: NE:sdoias._AUTHENTICATION_TYPE
title: AUTHENTICATION_TYPE (sdoias.h)
description: The values of the AUTHENTICATION_TYPE enumerated type are used to specify the authentication method.
helpviewer_keywords: ["AUTHENTICATION_TYPE","AUTHENTICATION_TYPE enumeration [Network Policy Server]","IAS_AUTH_ARAP","IAS_AUTH_CUSTOM","IAS_AUTH_EAP","IAS_AUTH_INVALID","IAS_AUTH_MD5CHAP","IAS_AUTH_MSCHAP","IAS_AUTH_MSCHAP2","IAS_AUTH_MSCHAP2_CPW","IAS_AUTH_MSCHAP_CPW","IAS_AUTH_NONE","IAS_AUTH_PAP","IAS_AUTH_PEAP","nps.sdo_authentication_type","nps.sdo_authenticationtype","sdo.authenticationtype","sdoias/AUTHENTICATION_TYPE","sdoias/IAS_AUTH_ARAP","sdoias/IAS_AUTH_CUSTOM","sdoias/IAS_AUTH_EAP","sdoias/IAS_AUTH_INVALID","sdoias/IAS_AUTH_MD5CHAP","sdoias/IAS_AUTH_MSCHAP","sdoias/IAS_AUTH_MSCHAP2","sdoias/IAS_AUTH_MSCHAP2_CPW","sdoias/IAS_AUTH_MSCHAP_CPW","sdoias/IAS_AUTH_NONE","sdoias/IAS_AUTH_PAP","sdoias/IAS_AUTH_PEAP"]
old-location: nps\sdo_authentication_type.htm
tech.root: Nps
ms.assetid: 55254986-8dfe-4ae1-84a1-3dc66b4e1190
ms.date: 12/05/2018
ms.keywords: AUTHENTICATION_TYPE, AUTHENTICATION_TYPE enumeration [Network Policy Server], IAS_AUTH_ARAP, IAS_AUTH_CUSTOM, IAS_AUTH_EAP, IAS_AUTH_INVALID, IAS_AUTH_MD5CHAP, IAS_AUTH_MSCHAP, IAS_AUTH_MSCHAP2, IAS_AUTH_MSCHAP2_CPW, IAS_AUTH_MSCHAP_CPW, IAS_AUTH_NONE, IAS_AUTH_PAP, IAS_AUTH_PEAP, nps.sdo_authentication_type, nps.sdo_authenticationtype, sdo.authenticationtype, sdoias/AUTHENTICATION_TYPE, sdoias/IAS_AUTH_ARAP, sdoias/IAS_AUTH_CUSTOM, sdoias/IAS_AUTH_EAP, sdoias/IAS_AUTH_INVALID, sdoias/IAS_AUTH_MD5CHAP, sdoias/IAS_AUTH_MSCHAP, sdoias/IAS_AUTH_MSCHAP2, sdoias/IAS_AUTH_MSCHAP2_CPW, sdoias/IAS_AUTH_MSCHAP_CPW, sdoias/IAS_AUTH_NONE, sdoias/IAS_AUTH_PAP, sdoias/IAS_AUTH_PEAP
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: AUTHENTICATION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AUTHENTICATION_TYPE
 - sdoias/_AUTHENTICATION_TYPE
 - AUTHENTICATION_TYPE
 - sdoias/AUTHENTICATION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SdoIas.h
api_name:
 - AUTHENTICATION_TYPE
---

# AUTHENTICATION_TYPE enumeration


## -description

The values of the <b>AUTHENTICATION_TYPE</b> enumerated 
    type are used to specify the authentication method.

## -enum-fields

### -field IAS_AUTH_INVALID:0

Specifies the authorization type as invalid.

### -field IAS_AUTH_PAP

Specifies the authorization type as PAP.

### -field IAS_AUTH_MD5CHAP

Specifies the authorization type as MD5CHAP.

### -field IAS_AUTH_MSCHAP

Specifies the authorization type as MSCHAP.

### -field IAS_AUTH_MSCHAP2

Specifies the authorization type as MSCHAP2.

### -field IAS_AUTH_EAP

Specifies the authorization type as EAP.

### -field IAS_AUTH_ARAP

Specifies the authorization type as PEAP.

### -field IAS_AUTH_NONE

Specifies that there is not authorization type.

### -field IAS_AUTH_CUSTOM

Specifies the authorization type as custom.

### -field IAS_AUTH_MSCHAP_CPW

Specifies the authorization type as <b>MSCHAP_CPW</b>.

### -field IAS_AUTH_MSCHAP2_CPW

Specifies the authorization type as <b>MSCHAP2_CPW</b>.

### -field IAS_AUTH_PEAP

Specifies the authorization type as <b>PEAP</b>.

## -see-also

<a href="/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties">IASCOMMONPROPERTIES</a>



<a href="/windows/desktop/api/sdoias/ne-sdoias-radiusproperties">RADIUSPROPERTIES</a>
