---
UID: NF:fhcfg.IFhReassociation.ValidateTarget
title: IFhReassociation::ValidateTarget (fhcfg.h)
description: This method checks whether a certain storage device or network share can be used as a File History default target and, thus, whether reassociation is possible at all or not.
helpviewer_keywords: ["FhReassociation class [Windows API]","ValidateTarget method","IFhReassociation interface [Windows API]","ValidateTarget method","IFhReassociation.ValidateTarget","IFhReassociation::ValidateTarget","ValidateTarget","ValidateTarget method [Windows API]","ValidateTarget method [Windows API]","FhReassociation class","ValidateTarget method [Windows API]","IFhReassociation interface","fhcfg/IFhReassociation::ValidateTarget","winprog.ifhreassociation_validatetarget"]
old-location: winprog\ifhreassociation_validatetarget.htm
tech.root: winprog
ms.assetid: 307F2C8F-B847-437C-BDD7-BE09FD407C79
ms.date: 12/05/2018
ms.keywords: FhReassociation class [Windows API],ValidateTarget method, IFhReassociation interface [Windows API],ValidateTarget method, IFhReassociation.ValidateTarget, IFhReassociation::ValidateTarget, ValidateTarget, ValidateTarget method [Windows API], ValidateTarget method [Windows API],FhReassociation class, ValidateTarget method [Windows API],IFhReassociation interface, fhcfg/IFhReassociation::ValidateTarget, winprog.ifhreassociation_validatetarget
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
 - IFhReassociation::ValidateTarget
 - fhcfg/IFhReassociation::ValidateTarget
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
 - IFhReassociation.ValidateTarget
 - FhReassociation.ValidateTarget
---

# IFhReassociation::ValidateTarget


## -description

 This method checks whether a certain storage device or network share can be used as a File History default target and, thus, whether reassociation is possible at all or not.

> [!NOTE] 
> **IFhReassociation** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param TargetUrl [in]

Specifies the storage device or network share to be validated.

### -param ValidationResult [out]

On return, contains a value specifying the result of the device validation. See  the <a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_device_validation_result">FH_DEVICE_VALIDATION_RESULT</a> enumeration for a detailed description of supported device validation results.

## -returns

<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

## -remarks

For local disks, the <i>TargetUrl</i> parameter contains the drive letter. This path must end with a trailing backslash (for example, "X:\\").

For network shares, the <i>TargetUrl</i> parameter contains the full path of the share.  This path must end with a trailing backslash (for example, "\\\\myserver\myshare\\").

## -see-also

<a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_device_validation_result">FH_DEVICE_VALIDATION_RESULT</a>



<a href="/windows/desktop/DevNotes/fhreassociation">FhReassociation</a>



<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhreassociation">IFhReassociation</a>