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

# _FH_TARGET_PROPERTY_TYPE enumeration


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
 

 

