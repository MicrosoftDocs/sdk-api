---
UID: NF:fhcfg.IFhConfigMgr.ProvisionAndSetNewTarget
title: IFhConfigMgr::ProvisionAndSetNewTarget (fhcfg.h)
description: Provisions a certain storage device or network share as a File History backup target and assigns it as the default backup target for the current user.
helpviewer_keywords: ["FhConfigMgr class [Windows API]","ProvisionAndSetNewTarget method","IFhConfigMgr interface [Windows API]","ProvisionAndSetNewTarget method","IFhConfigMgr.ProvisionAndSetNewTarget","IFhConfigMgr::ProvisionAndSetNewTarget","ProvisionAndSetNewTarget","ProvisionAndSetNewTarget method [Windows API]","ProvisionAndSetNewTarget method [Windows API]","FhConfigMgr class","ProvisionAndSetNewTarget method [Windows API]","IFhConfigMgr interface","fhcfg/IFhConfigMgr::ProvisionAndSetNewTarget","winprog.ifhconfigmgr_provisionandsetnewtarget"]
old-location: winprog\ifhconfigmgr_provisionandsetnewtarget.htm
tech.root: winprog
ms.assetid: 9C9FA696-CFB2-4814-96D5-2B9B6A2AB426
ms.date: 12/05/2018
ms.keywords: FhConfigMgr class [Windows API],ProvisionAndSetNewTarget method, IFhConfigMgr interface [Windows API],ProvisionAndSetNewTarget method, IFhConfigMgr.ProvisionAndSetNewTarget, IFhConfigMgr::ProvisionAndSetNewTarget, ProvisionAndSetNewTarget, ProvisionAndSetNewTarget method [Windows API], ProvisionAndSetNewTarget method [Windows API],FhConfigMgr class, ProvisionAndSetNewTarget method [Windows API],IFhConfigMgr interface, fhcfg/IFhConfigMgr::ProvisionAndSetNewTarget, winprog.ifhconfigmgr_provisionandsetnewtarget
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFhConfigMgr::ProvisionAndSetNewTarget
 - fhcfg/IFhConfigMgr::ProvisionAndSetNewTarget
dev_langs:
 - c++
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
---

# IFhConfigMgr::ProvisionAndSetNewTarget


## -description

Provisions a certain storage device or network share as a File History backup target and assigns it as the default backup target for the current user.

> [!NOTE] 
> **IFhConfigMgr** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param TargetUrl [in]

Specifies the storage device or network share to be provisioned and assigned as the default.

### -param TargetName [in]

Specifies a user-friendly name for the specified backup target.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code such as one of the values defined in the FhErrors.h header file.

## -remarks

For local disks, the <i>TargetUrl</i> parameter contains the drive letter. This path must end with a trailing backslash (for example, "X:\\").

For network shares, the <i>TargetUrl</i> parameter contains the full path of the share.  This path must end with a trailing backslash (for example, "\\\\myserver\myshare\\").

It is highly recommended that the storage device or network share specified by the <i>TargetUrl</i> parameter be validated first using the <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-validatetarget">IFhConfigMgr::ValidateTarget</a> method. If <b>ValidateTarget</b> returns a validation result other than <b>FH_VALID_TARGET</b>, assigning this storage device or network share as the default backup target may have unpredictable consequences.

## -see-also

<a href="/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhconfigmgr">IFhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-validatetarget">IFhConfigMgr::ValidateTarget</a>