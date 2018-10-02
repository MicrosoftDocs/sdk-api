---
UID: NE:sdoias._IASPROPERTIES
title: "_IASPROPERTIES"
author: windows-sdk-content
description: The values of the IASPROPERTIES enumeration type enumerate properties related to NPS.
old-location: nps\SDO_iasproperties.htm
tech.root: Nps
ms.assetid: 4290621c-7fc7-416b-89a2-11f2254f0d70
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IASPROPERTIES, IASPROPERTIES enumeration [Network Policy Server], PROPERTY_IAS_AUDITORS_COLLECTION, PROPERTY_IAS_POLICIES_COLLECTION, PROPERTY_IAS_PROFILES_COLLECTION, PROPERTY_IAS_PROTOCOLS_COLLECTION, PROPERTY_IAS_PROXYPOLICIES_COLLECTION, PROPERTY_IAS_PROXYPROFILES_COLLECTION, PROPERTY_IAS_RADIUSSERVERGROUPS_COLLECTION, PROPERTY_IAS_REMEDIATIONSERVERGROUPS_COLLECTION, PROPERTY_IAS_REQUESTHANDLERS_COLLECTION, PROPERTY_IAS_SHVTEMPLATES_COLLECTION, _IASPROPERTIES, _sdo_iasproperties, nps.SDO_iasproperties, sdo.iasproperties, sdoias/IASPROPERTIES, sdoias/PROPERTY_IAS_AUDITORS_COLLECTION, sdoias/PROPERTY_IAS_POLICIES_COLLECTION, sdoias/PROPERTY_IAS_PROFILES_COLLECTION, sdoias/PROPERTY_IAS_PROTOCOLS_COLLECTION, sdoias/PROPERTY_IAS_PROXYPOLICIES_COLLECTION, sdoias/PROPERTY_IAS_PROXYPROFILES_COLLECTION, sdoias/PROPERTY_IAS_RADIUSSERVERGROUPS_COLLECTION, sdoias/PROPERTY_IAS_REMEDIATIONSERVERGROUPS_COLLECTION, sdoias/PROPERTY_IAS_REQUESTHANDLERS_COLLECTION, sdoias/PROPERTY_IAS_SHVTEMPLATES_COLLECTION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SdoIas.h
api_name:
 - IASPROPERTIES
product: Windows
targetos: Windows
req.typenames: IASPROPERTIES
req.redist: 
---

# _IASPROPERTIES enumeration


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




<a href="https://msdn.microsoft.com/12cf768e-71b2-4b95-9b5a-2b9e3ce80f37">RADIUSPROXYPROPERTIES</a>



<a href="https://msdn.microsoft.com/b78aacfb-2e79-4c25-bc0c-acecb1a12993">RADIUSSERVERGROUPPROPERTIES</a>
 

 

