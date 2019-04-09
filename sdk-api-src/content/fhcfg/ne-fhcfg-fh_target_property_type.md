---
UID: NE:fhcfg._FH_TARGET_PROPERTY_TYPE
title: FH_TARGET_PROPERTY_TYPE (fhcfg.h)
author: windows-sdk-content
description: Specifies the type of a property of a backup target.
old-location: winprog\fh_target_property_type.htm
tech.root: DevNotes
ms.assetid: 0A39626B-942F-4BD6-930D-15E9D401F0FF
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PFH_TARGET_PROPERTY_TYPE, FH_TARGET_DRIVE_TYPE, FH_TARGET_NAME, FH_TARGET_PROPERTY_TYPE, FH_TARGET_PROPERTY_TYPE enumeration [Windows API], FH_TARGET_URL, MAX_TARGET_PROPERTY, fhcfg/FH_TARGET_DRIVE_TYPE, fhcfg/FH_TARGET_NAME, fhcfg/FH_TARGET_PROPERTY_TYPE, fhcfg/FH_TARGET_URL, fhcfg/MAX_TARGET_PROPERTY, winprog.fh_target_property_type"
ms.topic: enum
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
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
 - Fhcfg.h
api_name:
 - FH_TARGET_PROPERTY_TYPE
product: Windows
targetos: Windows
req.typenames: FH_TARGET_PROPERTY_TYPE, *PFH_TARGET_PROPERTY_TYPE
req.redist: 
---

# FH_TARGET_PROPERTY_TYPE enumeration


## -description


Specifies the type of a property of a backup target.


## -enum-fields




### -field FH_TARGET_NAME

The property is a string that contains the backup target’s friendly name.  The friendly name is set during target provisioning by calling the <a href="https://msdn.microsoft.com/9C9FA696-CFB2-4814-96D5-2B9B6A2AB426">IFhConfigMgr::ProvisionAndSetNewTarget</a> method.


### -field FH_TARGET_URL

The property is a string that contains a path to the backup target.


### -field FH_TARGET_DRIVE_TYPE

The property is a numeric property that specifies the target type of the backup target. See the <a href="https://msdn.microsoft.com/4D3F3B57-BD6E-4334-8DF6-ECD317A051EC">FH_TARGET_DRIVE_TYPES</a> enumeration for the list of possible backup target types.


### -field MAX_TARGET_PROPERTY

The maximum enumeration value for this enumeration. This value and all values greater than it are reserved for system use.


## -remarks



To query a backup target property, call the <a href="https://msdn.microsoft.com/DC5FE023-FA6E-4B97-AD9D-830975A17159">IFhTarget::GetStringProperty</a> method or the <a href="https://msdn.microsoft.com/3FA2F3AB-A406-4F19-AA5A-0D5596F1BF2C">IFhTarget::GetNumericalProperty</a> method.

For local disks, the <b>FH_TARGET_URL</b> property contains the drive letter. This path must end with a trailing backslash (for example, "X:\").

For network shares, the <b>FH_TARGET_URL</b> property contains the full path of the share.  This path must end with a trailing backslash (for example, "\\myserver\myshare\").




## -see-also




<a href="https://msdn.microsoft.com/4D3F3B57-BD6E-4334-8DF6-ECD317A051EC">FH_TARGET_DRIVE_TYPES</a>



<a href="https://msdn.microsoft.com/9C9FA696-CFB2-4814-96D5-2B9B6A2AB426">IFhConfigMgr::ProvisionAndSetNewTarget</a>



<a href="https://msdn.microsoft.com/3FA2F3AB-A406-4F19-AA5A-0D5596F1BF2C">IFhTarget::GetNumericalProperty</a>



<a href="https://msdn.microsoft.com/DC5FE023-FA6E-4B97-AD9D-830975A17159">IFhTarget::GetStringProperty</a>
 

 

