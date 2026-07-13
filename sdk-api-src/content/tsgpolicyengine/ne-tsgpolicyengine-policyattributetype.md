---
UID: NE:tsgpolicyengine.__MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0005
title: PolicyAttributeType (tsgpolicyengine.h)
description: Specifies the redirection settings associated with a connection.
helpviewer_keywords: ["AllowOnlySDRServers","ClipboardRedirectionDisabled","DisableAllRedirections","DriveRedirectionDisabled","EnableAllRedirections","PnpRedirectionDisabled","PolicyAttributeType","PolicyAttributeType enumeration [Remote Desktop Services]","PortRedirectionDisabled","PrinterRedirectionDisabled","termserv.policyattributetype","tsgpolicyengine/AllowOnlySDRServers","tsgpolicyengine/ClipboardRedirectionDisabled","tsgpolicyengine/DisableAllRedirections","tsgpolicyengine/DriveRedirectionDisabled","tsgpolicyengine/EnableAllRedirections","tsgpolicyengine/PnpRedirectionDisabled","tsgpolicyengine/PolicyAttributeType","tsgpolicyengine/PortRedirectionDisabled","tsgpolicyengine/PrinterRedirectionDisabled"]
old-location: termserv\policyattributetype.htm
tech.root: TermServ
ms.assetid: e2e53f33-1fc5-4002-81ed-8c9cce58f28e
ms.date: 12/05/2018
ms.keywords: AllowOnlySDRServers, ClipboardRedirectionDisabled, DisableAllRedirections, DriveRedirectionDisabled, EnableAllRedirections, PnpRedirectionDisabled, PolicyAttributeType, PolicyAttributeType enumeration [Remote Desktop Services], PortRedirectionDisabled, PrinterRedirectionDisabled, termserv.policyattributetype, tsgpolicyengine/AllowOnlySDRServers, tsgpolicyengine/ClipboardRedirectionDisabled, tsgpolicyengine/DisableAllRedirections, tsgpolicyengine/DriveRedirectionDisabled, tsgpolicyengine/EnableAllRedirections, tsgpolicyengine/PnpRedirectionDisabled, tsgpolicyengine/PolicyAttributeType, tsgpolicyengine/PortRedirectionDisabled, tsgpolicyengine/PrinterRedirectionDisabled
req.header: tsgpolicyengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TSGPolicyEngine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PolicyAttributeType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0005
 - tsgpolicyengine/__MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0005
 - PolicyAttributeType
 - tsgpolicyengine/PolicyAttributeType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - TSGPolicyEngine.h
api_name:
 - PolicyAttributeType
---

# PolicyAttributeType enumeration


## -description

Specifies the redirection settings associated with a connection.

## -enum-fields

### -field EnableAllRedirections:0

Enable device redirection for all devices.

### -field DisableAllRedirections

Disable device redirection for all devices.

### -field DriveRedirectionDisabled

Disable drive redirection.

### -field PrinterRedirectionDisabled

Disable printer redirection.

### -field PortRedirectionDisabled

Disable port redirection.

### -field ClipboardRedirectionDisabled

Disable clipboard redirection.

### -field PnpRedirectionDisabled

Disable Plug and Play device redirection.

### -field AllowOnlySDRServers

Only allow connections to servers that support secure device redirection.

