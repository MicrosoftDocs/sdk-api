---
UID: NF:fhcfg.IFhConfigMgr.ValidateTarget
title: IFhConfigMgr::ValidateTarget (fhcfg.h)
description: Checks whether a certain storage device or network share can be used as a File History backup target.
helpviewer_keywords: ["FhConfigMgr class [Windows API]","ValidateTarget method","IFhConfigMgr interface [Windows API]","ValidateTarget method","IFhConfigMgr.ValidateTarget","IFhConfigMgr::ValidateTarget","ValidateTarget","ValidateTarget method [Windows API]","ValidateTarget method [Windows API]","FhConfigMgr class","ValidateTarget method [Windows API]","IFhConfigMgr interface","fhcfg/IFhConfigMgr::ValidateTarget","winprog.ifhconfigmgr_validatetarget"]
old-location: winprog\ifhconfigmgr_validatetarget.htm
tech.root: winprog
ms.assetid: EC41C4EE-A909-4DD4-AA32-5054BBEAF421
ms.date: 12/05/2018
ms.keywords: FhConfigMgr class [Windows API],ValidateTarget method, IFhConfigMgr interface [Windows API],ValidateTarget method, IFhConfigMgr.ValidateTarget, IFhConfigMgr::ValidateTarget, ValidateTarget, ValidateTarget method [Windows API], ValidateTarget method [Windows API],FhConfigMgr class, ValidateTarget method [Windows API],IFhConfigMgr interface, fhcfg/IFhConfigMgr::ValidateTarget, winprog.ifhconfigmgr_validatetarget
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
 - IFhConfigMgr::ValidateTarget
 - fhcfg/IFhConfigMgr::ValidateTarget
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
 - IFhConfigMgr.ValidateTarget
 - FhConfigMgr.ValidateTarget
---

# IFhConfigMgr::ValidateTarget


## -description

 Checks whether a certain storage device or network share can be used as a File History backup target.

> [!NOTE] 
> **IFhConfigMgr** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param TargetUrl [in]

The storage device or network share to be validated.

### -param ValidationResult [out]

Receives the result of the device validation. See the <a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_device_validation_result">FH_DEVICE_VALIDATION_RESULT</a> enumeration for the list of possible device validation result values.

## -returns

<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

## -remarks

For local disks, the <i>TargetUrl</i> parameter contains the drive letter. This path must end with a trailing backslash (for example, "X:\\").

For network shares, the <i>TargetUrl</i> parameter contains the full path of the share.  This path must end with a trailing backslash (for example, "\\\\myserver\myshare\\").

## -see-also

<a href="/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhconfigmgr">IFhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-getdefaulttarget">IFhConfigMgr::GetDefaultTarget</a>