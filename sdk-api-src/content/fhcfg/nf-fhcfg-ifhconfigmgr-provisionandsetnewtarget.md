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

# IFhConfigMgr::ProvisionAndSetNewTarget


## -description


Provisions a certain storage device or network share as a File History backup target and assigns it as the default backup target for the current user.


## -parameters




### -param TargetUrl [in]

Specifies the storage device or network share to be provisioned and assigned as the default.


### -param TargetName [in]

Specifies a user-friendly name for the specified backup target.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code such as one of the values defined in the FhErrors.h header file.




## -remarks



For local disks, the <i>TargetUrl</i> parameter contains the drive letter. This path must end with a trailing backslash (for example, "X:\").

For network shares, the <i>TargetUrl</i> parameter contains the full path of the share.  This path must end with a trailing backslash (for example, "\\myserver\myshare\").

It is highly recommended that the storage device or network share specified by the <i>TargetUrl</i> parameter be validated first using the <a href="https://msdn.microsoft.com/EC41C4EE-A909-4DD4-AA32-5054BBEAF421">IFhConfigMgr::ValidateTarget</a> method. If <b>ValidateTarget</b> returns a validation result other than <b>FH_VALID_TARGET</b>, assigning this storage device or network share as the default backup target may have unpredictable consequences.




## -see-also




<a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a>



<a href="https://msdn.microsoft.com/CDE8A011-6E78-49DF-A5E1-8E968355BA11">IFhConfigMgr</a>



<a href="https://msdn.microsoft.com/EC41C4EE-A909-4DD4-AA32-5054BBEAF421">IFhConfigMgr::ValidateTarget</a>
 

 

