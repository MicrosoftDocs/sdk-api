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

# __MIDL___MIDL_itf_ads_0001_0048_0003 enumeration


## -description


The <b>ADS_ACEFLAG_ENUM</b> enumeration is used to specify the behavior of an Access Control Entry (ACE) for an Active Directory object.

For more information and possible values for file, file share and registry objects, see the <b>AceFlags</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538847">ACE_HEADER</a> structure.


## -enum-fields




### -field ADS_ACEFLAG_INHERIT_ACE

Child objects will inherit this access-control entry (ACE). The inherited ACE is inheritable unless the ADS_ACEFLAG_NO_PROPAGATE_INHERIT_ACE flag is set.


### -field ADS_ACEFLAG_NO_PROPAGATE_INHERIT_ACE

The system will clear the ADS_ACEFLAG_INHERIT_ACE flag for the inherited ACEs of child objects. This prevents the ACE from being inherited by subsequent generations of objects.


### -field ADS_ACEFLAG_INHERIT_ONLY_ACE

Indicates that an inherit-only ACE that does not exercise access control on the object to which it is attached. If this flag is not set, the ACE is an effective ACE that exerts access control on the object to which it is attached.


### -field ADS_ACEFLAG_INHERITED_ACE

Indicates whether or not the ACE was inherited. The system sets this bit.


### -field ADS_ACEFLAG_VALID_INHERIT_FLAGS

Indicates whether the inherit flags are valid. The system sets this bit.


### -field ADS_ACEFLAG_SUCCESSFUL_ACCESS

Generates audit messages for successful access attempts, used with ACEs that audit the system in a system access-control list (SACL).


### -field ADS_ACEFLAG_FAILED_ACCESS

Generates audit messages for failed access attempts, used with ACEs that audit the system in a SACL.


## -remarks



Because VBScript cannot read data from a type library, VBScript applications do not understand the symbolic constants as defined in these enumerations. You should use the numerical constants instead to set the appropriate flags in your VBScript applications. If you want to use the symbolic constants as a good programming practice, write explicit declarations of such constants, as done here, in your VBScript applications.




## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI Enumerations</a>



<a href="https://msdn.microsoft.com/1884efe5-86f5-4579-a25e-2ff9c9a6ec2a">IADsObjectOptions</a>



<a href="https://msdn.microsoft.com/1672c1b0-1008-41e7-8ca4-eefb559f523d">IADsPathname::Set</a>
 

 

