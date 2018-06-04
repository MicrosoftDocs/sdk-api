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

# __MIDL___MIDL_itf_ads_0001_0048_0005 enumeration


## -description


The <b>ADS_SD_CONTROL_ENUM</b> enumeration specifies control flags for a security descriptor.


## -enum-fields




### -field ADS_SD_CONTROL_SE_OWNER_DEFAULTED

A default mechanism provides the owner security identifier (SID) of the security descriptor rather than the original provider of the security descriptor.


### -field ADS_SD_CONTROL_SE_GROUP_DEFAULTED

A default mechanism provides the group SID of the security descriptor rather than the original provider of the security descriptor.


### -field ADS_SD_CONTROL_SE_DACL_PRESENT

The discretionary access-control list (DACL) is present in the security descriptor. If this flag is not set, or if this flag is set and the DACL is <b>NULL</b>, the security descriptor allows full access to everyone.


### -field ADS_SD_CONTROL_SE_DACL_DEFAULTED

The security descriptor uses a default DACL built from the creator's access token.


### -field ADS_SD_CONTROL_SE_SACL_PRESENT

The system access-control list (SACL) is present in the security descriptor.


### -field ADS_SD_CONTROL_SE_SACL_DEFAULTED

The security descriptor uses a default SACL built from the creator's access token.


### -field ADS_SD_CONTROL_SE_DACL_AUTO_INHERIT_REQ

THE DACL of the security descriptor must be inherited.


### -field ADS_SD_CONTROL_SE_SACL_AUTO_INHERIT_REQ

The SACL of the security descriptor must be inherited.


### -field ADS_SD_CONTROL_SE_DACL_AUTO_INHERITED

The DACL of the security descriptor supports automatic propagation of inheritable access-control entries (ACEs) to existing child objects.


### -field ADS_SD_CONTROL_SE_SACL_AUTO_INHERITED

The SACL of the security descriptor supports automatic propagation of inheritable ACEs to existing child objects.


### -field ADS_SD_CONTROL_SE_DACL_PROTECTED

The security descriptor will not allow inheritable ACEs to modify the DACL.


### -field ADS_SD_CONTROL_SE_SACL_PROTECTED

The security descriptor will not allow inheritable ACEs to modify the SACL.


### -field ADS_SD_CONTROL_SE_SELF_RELATIVE

The security descriptor is of self-relative format with all the security information in a continuous block of memory.


## -remarks



For more information, see  <a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a> under Security in the Platform Software Development Kit (SDK).

Since VBScript cannot read information from a type library, VBScript applications do not understand the symbolic constants as defined above. You should use the numerical constants instead to set the appropriate flags in your VBScript applications. If you want to use the symbolic constants as a good programming practice, you should make explicit declarations of such constants, as done here, in your VBScript applications.




## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI Enumerations</a>



<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>
 

 

