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

# _POLICYPROPERTIES enumeration


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




<a href="https://msdn.microsoft.com/09cb8457-9baf-4139-ba80-6eb608db6a65">CONDITIONPROPERTIES</a>
 

 

