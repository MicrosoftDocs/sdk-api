---
UID: NE:sdoias._IASPROPERTIES
title: IASPROPERTIES (sdoias.h)
description: The values of the IASPROPERTIES enumeration type enumerate properties related to NPS.
helpviewer_keywords: ["IASPROPERTIES","IASPROPERTIES enumeration [Network Policy Server]","PROPERTY_IAS_AUDITORS_COLLECTION","PROPERTY_IAS_POLICIES_COLLECTION","PROPERTY_IAS_PROFILES_COLLECTION","PROPERTY_IAS_PROTOCOLS_COLLECTION","PROPERTY_IAS_PROXYPOLICIES_COLLECTION","PROPERTY_IAS_PROXYPROFILES_COLLECTION","PROPERTY_IAS_RADIUSSERVERGROUPS_COLLECTION","PROPERTY_IAS_REMEDIATIONSERVERGROUPS_COLLECTION","PROPERTY_IAS_REQUESTHANDLERS_COLLECTION","PROPERTY_IAS_SHVTEMPLATES_COLLECTION","_sdo_iasproperties","nps.SDO_iasproperties","sdo.iasproperties","sdoias/IASPROPERTIES","sdoias/PROPERTY_IAS_AUDITORS_COLLECTION","sdoias/PROPERTY_IAS_POLICIES_COLLECTION","sdoias/PROPERTY_IAS_PROFILES_COLLECTION","sdoias/PROPERTY_IAS_PROTOCOLS_COLLECTION","sdoias/PROPERTY_IAS_PROXYPOLICIES_COLLECTION","sdoias/PROPERTY_IAS_PROXYPROFILES_COLLECTION","sdoias/PROPERTY_IAS_RADIUSSERVERGROUPS_COLLECTION","sdoias/PROPERTY_IAS_REMEDIATIONSERVERGROUPS_COLLECTION","sdoias/PROPERTY_IAS_REQUESTHANDLERS_COLLECTION","sdoias/PROPERTY_IAS_SHVTEMPLATES_COLLECTION"]
old-location: nps\SDO_iasproperties.htm
tech.root: Nps
ms.assetid: 4290621c-7fc7-416b-89a2-11f2254f0d70
ms.date: 12/05/2018
ms.keywords: IASPROPERTIES, IASPROPERTIES enumeration [Network Policy Server], PROPERTY_IAS_AUDITORS_COLLECTION, PROPERTY_IAS_POLICIES_COLLECTION, PROPERTY_IAS_PROFILES_COLLECTION, PROPERTY_IAS_PROTOCOLS_COLLECTION, PROPERTY_IAS_PROXYPOLICIES_COLLECTION, PROPERTY_IAS_PROXYPROFILES_COLLECTION, PROPERTY_IAS_RADIUSSERVERGROUPS_COLLECTION, PROPERTY_IAS_REMEDIATIONSERVERGROUPS_COLLECTION, PROPERTY_IAS_REQUESTHANDLERS_COLLECTION, PROPERTY_IAS_SHVTEMPLATES_COLLECTION, _sdo_iasproperties, nps.SDO_iasproperties, sdo.iasproperties, sdoias/IASPROPERTIES, sdoias/PROPERTY_IAS_AUDITORS_COLLECTION, sdoias/PROPERTY_IAS_POLICIES_COLLECTION, sdoias/PROPERTY_IAS_PROFILES_COLLECTION, sdoias/PROPERTY_IAS_PROTOCOLS_COLLECTION, sdoias/PROPERTY_IAS_PROXYPOLICIES_COLLECTION, sdoias/PROPERTY_IAS_PROXYPROFILES_COLLECTION, sdoias/PROPERTY_IAS_RADIUSSERVERGROUPS_COLLECTION, sdoias/PROPERTY_IAS_REMEDIATIONSERVERGROUPS_COLLECTION, sdoias/PROPERTY_IAS_REQUESTHANDLERS_COLLECTION, sdoias/PROPERTY_IAS_SHVTEMPLATES_COLLECTION
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
req.typenames: IASPROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IASPROPERTIES
 - sdoias/_IASPROPERTIES
 - IASPROPERTIES
 - sdoias/IASPROPERTIES
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
 - IASPROPERTIES
---

# IASPROPERTIES enumeration


## -description

<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008. The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The values of the 
<b>IASPROPERTIES</b> enumeration type enumerate properties related to NPS.

## -enum-fields

### -field PROPERTY_IAS_RADIUSSERVERGROUPS_COLLECTION

The collection of RADIUS server groups.

### -field PROPERTY_IAS_POLICIES_COLLECTION

The collection of Network Access Policies (NAP).

### -field PROPERTY_IAS_PROFILES_COLLECTION

The collection of profiles for the network access policies.

### -field PROPERTY_IAS_PROTOCOLS_COLLECTION

The collection of protocols used by NPS.

### -field PROPERTY_IAS_AUDITORS_COLLECTION

The collection of auditors used by NPS.

### -field PROPERTY_IAS_REQUESTHANDLERS_COLLECTION

The collection of request handlers used by NPS.

### -field PROPERTY_IAS_PROXYPOLICIES_COLLECTION

The collection of Network Access Policies for connection request processing.

### -field PROPERTY_IAS_PROXYPROFILES_COLLECTION

The collection of profiles for connection request processing.

### -field PROPERTY_IAS_REMEDIATIONSERVERGROUPS_COLLECTION

Used by the Remediation Server settings of NPS user interface.

### -field PROPERTY_IAS_SHVTEMPLATES_COLLECTION

Used by the System Health Validator Template settings of NPS user interface.

## -see-also

<a href="/windows/desktop/api/sdoias/ne-sdoias-radiusproxyproperties">RADIUSPROXYPROPERTIES</a>



<a href="/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties">RADIUSSERVERGROUPPROPERTIES</a>