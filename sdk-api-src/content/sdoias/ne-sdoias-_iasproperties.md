---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

