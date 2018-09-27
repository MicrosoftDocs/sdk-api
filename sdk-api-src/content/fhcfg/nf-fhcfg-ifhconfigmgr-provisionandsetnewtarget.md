---
UID: NF:fhcfg.IFhConfigMgr.ProvisionAndSetNewTarget
title: IFhConfigMgr::ProvisionAndSetNewTarget
author: windows-sdk-content
description: Provisions a certain storage device or network share as a File History backup target and assigns it as the default backup target for the current user.
old-location: winprog\ifhconfigmgr_provisionandsetnewtarget.htm
tech.root: devnotes
ms.assetid: 9C9FA696-CFB2-4814-96D5-2B9B6A2AB426
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: FhConfigMgr class [Windows API],ProvisionAndSetNewTarget method, IFhConfigMgr interface [Windows API],ProvisionAndSetNewTarget method, IFhConfigMgr.ProvisionAndSetNewTarget, IFhConfigMgr::ProvisionAndSetNewTarget, ProvisionAndSetNewTarget, ProvisionAndSetNewTarget method [Windows API], ProvisionAndSetNewTarget method [Windows API],FhConfigMgr class, ProvisionAndSetNewTarget method [Windows API],IFhConfigMgr interface, fhcfg/IFhConfigMgr::ProvisionAndSetNewTarget, winprog.ifhconfigmgr_provisionandsetnewtarget
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - COM
api_location:
 - Fhcfg.h
api_name:
 - IFhConfigMgr.ProvisionAndSetNewTarget
 - FhConfigMgr.ProvisionAndSetNewTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

