---
UID: NE:sdoias._POLICYPROPERTIES
title: POLICYPROPERTIES (sdoias.h)
description: The values of the POLICYPROPERTIES enumeration type enumerate properties of a Network Access Policy (NAP).
helpviewer_keywords: ["POLICYPROPERTIES","POLICYPROPERTIES enumeration [Network Policy Server]","PROPERTY_POLICY_ACTION","PROPERTY_POLICY_CONDITIONS_COLLECTION","PROPERTY_POLICY_CONSTRAINT","PROPERTY_POLICY_ENABLED","PROPERTY_POLICY_MERIT","PROPERTY_POLICY_PROFILE_NAME","PROPERTY_POLICY_SOURCETAG","PROPERTY_POLICY_UNUSED0","PROPERTY_POLICY_UNUSED1","_sdo_policyproperties","nps.SDO_policyproperties","sdo.policyproperties","sdoias/POLICYPROPERTIES","sdoias/PROPERTY_POLICY_ACTION","sdoias/PROPERTY_POLICY_CONDITIONS_COLLECTION","sdoias/PROPERTY_POLICY_CONSTRAINT","sdoias/PROPERTY_POLICY_ENABLED","sdoias/PROPERTY_POLICY_MERIT","sdoias/PROPERTY_POLICY_PROFILE_NAME","sdoias/PROPERTY_POLICY_SOURCETAG","sdoias/PROPERTY_POLICY_UNUSED0","sdoias/PROPERTY_POLICY_UNUSED1"]
old-location: nps\SDO_policyproperties.htm
tech.root: Nps
ms.assetid: 1e12baf8-e1f4-4b46-ba08-58adf4f3012e
ms.date: 12/05/2018
ms.keywords: POLICYPROPERTIES, POLICYPROPERTIES enumeration [Network Policy Server], PROPERTY_POLICY_ACTION, PROPERTY_POLICY_CONDITIONS_COLLECTION, PROPERTY_POLICY_CONSTRAINT, PROPERTY_POLICY_ENABLED, PROPERTY_POLICY_MERIT, PROPERTY_POLICY_PROFILE_NAME, PROPERTY_POLICY_SOURCETAG, PROPERTY_POLICY_UNUSED0, PROPERTY_POLICY_UNUSED1, _sdo_policyproperties, nps.SDO_policyproperties, sdo.policyproperties, sdoias/POLICYPROPERTIES, sdoias/PROPERTY_POLICY_ACTION, sdoias/PROPERTY_POLICY_CONDITIONS_COLLECTION, sdoias/PROPERTY_POLICY_CONSTRAINT, sdoias/PROPERTY_POLICY_ENABLED, sdoias/PROPERTY_POLICY_MERIT, sdoias/PROPERTY_POLICY_PROFILE_NAME, sdoias/PROPERTY_POLICY_SOURCETAG, sdoias/PROPERTY_POLICY_UNUSED0, sdoias/PROPERTY_POLICY_UNUSED1
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
req.typenames: POLICYPROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _POLICYPROPERTIES
 - sdoias/_POLICYPROPERTIES
 - POLICYPROPERTIES
 - sdoias/POLICYPROPERTIES
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
 - POLICYPROPERTIES
---

# POLICYPROPERTIES enumeration


## -description

The values of the <b>POLICYPROPERTIES</b> enumeration type enumerate properties of a 
    Network Access Policy (NAP).

## -enum-fields

### -field PROPERTY_POLICY_CONSTRAINT

String that contains all the text of the conditions.

Do not use this property to access the Conditions; use the 
       <b>PROPERTY_POLICY_CONDITIONS_COLLECTION</b> instead.

### -field PROPERTY_POLICY_MERIT

Specifies the relative position of this policy with respect to other policies.

In the UI, the upper-most policy in the UI has a merit value of 1, the next one down has a merit value of 2, 
       and so on.

You cannot set the merit value of a policy when you first create the object. A new policy object is always 
       applied in the same merit location. To order your policies, create the policy object and set its values. Apply 
       all the changes to the object, and then set the appropriate merit value and apply the changes.

### -field PROPERTY_POLICY_UNUSED0

This property is reserved.

### -field PROPERTY_POLICY_UNUSED1

This property is reserved.

### -field PROPERTY_POLICY_PROFILE_NAME

Specifies the profile name. This property is used by the system to associate the policy with the 
      profile.

### -field PROPERTY_POLICY_ACTION

Specifies the name of the profile associated with the policy. This property is not currently used. Use 
      <b>PROPERTY_POLICY_PROFILE_NAME</b> instead.

### -field PROPERTY_POLICY_CONDITIONS_COLLECTION

Specifies the conditions for this network access policy.

### -field PROPERTY_POLICY_ENABLED

Used by NPS user interface in policy evaluation. If the policy is not enabled, its configuration is present 
       but it is not applied.

### -field PROPERTY_POLICY_SOURCETAG

Used by NPS user interface to tag a set of policies to be applicable only for a specified kind of RADIUS 
       client (or source). For example, a policy tagged by "DHCP Server."

## -remarks

To create a new policy, you must specify a unique name for the policy, a profile to associate with the policy, 
    and a collection of conditions for the policy. The name of the policy and the name of the profile should be 
    identical.

## -see-also

<a href="/windows/desktop/api/sdoias/ne-sdoias-conditionproperties">CONDITIONPROPERTIES</a>