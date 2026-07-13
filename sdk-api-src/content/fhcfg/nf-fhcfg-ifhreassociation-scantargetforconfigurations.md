---
UID: NF:fhcfg.IFhReassociation.ScanTargetForConfigurations
title: IFhReassociation::ScanTargetForConfigurations (fhcfg.h)
description: Scans the namespace on a specified storage device or network share for File History configurations that can be reassociated with and continued to be used on the current computer.
helpviewer_keywords: ["FhReassociation class [Windows API]","ScanTargetForConfigurations method","IFhReassociation interface [Windows API]","ScanTargetForConfigurations method","IFhReassociation.ScanTargetForConfigurations","IFhReassociation::ScanTargetForConfigurations","ScanTargetForConfigurations","ScanTargetForConfigurations method [Windows API]","ScanTargetForConfigurations method [Windows API]","FhReassociation class","ScanTargetForConfigurations method [Windows API]","IFhReassociation interface","fhcfg/IFhReassociation::ScanTargetForConfigurations","winprog.ifhreassociation_scantargetforconfigurations"]
old-location: winprog\ifhreassociation_scantargetforconfigurations.htm
tech.root: winprog
ms.assetid: E26F5C41-50E7-4D4F-A6FF-D1B21AF28A9D
ms.date: 12/05/2018
ms.keywords: FhReassociation class [Windows API],ScanTargetForConfigurations method, IFhReassociation interface [Windows API],ScanTargetForConfigurations method, IFhReassociation.ScanTargetForConfigurations, IFhReassociation::ScanTargetForConfigurations, ScanTargetForConfigurations, ScanTargetForConfigurations method [Windows API], ScanTargetForConfigurations method [Windows API],FhReassociation class, ScanTargetForConfigurations method [Windows API],IFhReassociation interface, fhcfg/IFhReassociation::ScanTargetForConfigurations, winprog.ifhreassociation_scantargetforconfigurations
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
 - IFhReassociation::ScanTargetForConfigurations
 - fhcfg/IFhReassociation::ScanTargetForConfigurations
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
 - IFhReassociation.ScanTargetForConfigurations
 - FhReassociation.ScanTargetForConfigurations
---

# IFhReassociation::ScanTargetForConfigurations


## -description

Scans the namespace on a specified storage device or network share for File History configurations that can be reassociated with and continued to be used on the current computer.

> [!NOTE] 
> **IFhReassociation** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param TargetUrl [in]

Specifies the storage device or network share to be scanned.

## -returns

<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

If no File History configurations were found on the specified storage device or network share, the <code>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</code> error code is returned.

## -remarks

For local disks, the <i>TargetUrl</i> parameter contains the drive letter. This path must end with a trailing backslash (for example, "X:\\").

For network shares, the <i>TargetUrl</i> parameter contains the full path of the share.  This path must end with a trailing backslash (for example, "\\\\myserver\myshare\\").

## -see-also

<a href="/windows/desktop/DevNotes/fhreassociation">FhReassociation</a>



<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhreassociation">IFhReassociation</a>