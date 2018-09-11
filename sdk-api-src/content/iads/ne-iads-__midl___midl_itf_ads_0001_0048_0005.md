---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0048_0005
title: "__MIDL___MIDL_itf_ads_0001_0048_0005"
author: windows-sdk-content
description: The ADS_SD_CONTROL_ENUM enumeration specifies control flags for a security descriptor.
old-location: adsi\ads_sd_control_enum.htm
tech.root: ADSI
ms.assetid: e34ddf53-c7c6-41b0-93e7-cf47152c77be
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ADS_SD_CONTROL_ENUM, ADS_SD_CONTROL_ENUM enumeration [ADSI], ADS_SD_CONTROL_SE_DACL_AUTO_INHERITED, ADS_SD_CONTROL_SE_DACL_AUTO_INHERIT_REQ, ADS_SD_CONTROL_SE_DACL_DEFAULTED, ADS_SD_CONTROL_SE_DACL_PRESENT, ADS_SD_CONTROL_SE_DACL_PROTECTED, ADS_SD_CONTROL_SE_GROUP_DEFAULTED, ADS_SD_CONTROL_SE_OWNER_DEFAULTED, ADS_SD_CONTROL_SE_SACL_AUTO_INHERITED, ADS_SD_CONTROL_SE_SACL_AUTO_INHERIT_REQ, ADS_SD_CONTROL_SE_SACL_DEFAULTED, ADS_SD_CONTROL_SE_SACL_PRESENT, ADS_SD_CONTROL_SE_SACL_PROTECTED, ADS_SD_CONTROL_SE_SELF_RELATIVE, __MIDL___MIDL_itf_ads_0001_0048_0005, _ds_ads_sd_control_enum, adsi.ads__sd__control__enum, adsi.ads_sd_control_enum, iads/ADS_SD_CONTROL_ENUM, iads/ADS_SD_CONTROL_SE_DACL_AUTO_INHERITED, iads/ADS_SD_CONTROL_SE_DACL_AUTO_INHERIT_REQ, iads/ADS_SD_CONTROL_SE_DACL_DEFAULTED, iads/ADS_SD_CONTROL_SE_DACL_PRESENT, iads/ADS_SD_CONTROL_SE_DACL_PROTECTED, iads/ADS_SD_CONTROL_SE_GROUP_DEFAULTED, iads/ADS_SD_CONTROL_SE_OWNER_DEFAULTED, iads/ADS_SD_CONTROL_SE_SACL_AUTO_INHERITED, iads/ADS_SD_CONTROL_SE_SACL_AUTO_INHERIT_REQ, iads/ADS_SD_CONTROL_SE_SACL_DEFAULTED, iads/ADS_SD_CONTROL_SE_SACL_PRESENT, iads/ADS_SD_CONTROL_SE_SACL_PROTECTED, iads/ADS_SD_CONTROL_SE_SELF_RELATIVE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_SD_CONTROL_ENUM
product: Windows
targetos: Windows
req.typenames: ADS_SD_CONTROL_ENUM
req.redist: 
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
 

 

