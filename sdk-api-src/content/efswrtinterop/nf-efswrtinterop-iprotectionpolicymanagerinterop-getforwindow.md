---
UID: NF:efswrtinterop.IProtectionPolicyManagerInterop.GetForWindow
title: IProtectionPolicyManagerInterop::GetForWindow (efswrtinterop.h)
description: Returns the protection policy manager object associated with the current app window.
helpviewer_keywords: ["EDP.iprotectionpolicymanager_getforwindow","GetForWindow","GetForWindow method","GetForWindow method","IProtectionPolicyManagerInterop interface","IProtectionPolicyManagerInterop interface","GetForWindow method","IProtectionPolicyManagerInterop.GetForWindow","IProtectionPolicyManagerInterop::GetForWindow","efswrtinterop/IProtectionPolicyManagerInterop::GetForWindow"]
old-location: edp\iprotectionpolicymanager_getforwindow.htm
tech.root: EDP
ms.assetid: 638316E0-8D5C-4966-A44F-8F31ECBE83EB
ms.date: 12/05/2018
ms.keywords: EDP.iprotectionpolicymanager_getforwindow, GetForWindow, GetForWindow method, GetForWindow method,IProtectionPolicyManagerInterop interface, IProtectionPolicyManagerInterop interface,GetForWindow method, IProtectionPolicyManagerInterop.GetForWindow, IProtectionPolicyManagerInterop::GetForWindow, efswrtinterop/IProtectionPolicyManagerInterop::GetForWindow
req.header: efswrtinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Efswrtinterop.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Efswrt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IProtectionPolicyManagerInterop::GetForWindow
 - efswrtinterop/IProtectionPolicyManagerInterop::GetForWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - efswrt.dll
api_name:
 - IProtectionPolicyManagerInterop.GetForWindow
---

# IProtectionPolicyManagerInterop::GetForWindow


## -description

<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy can be applied on Windows 10, version 1607.</div>
<div> </div>Returns the protection policy manager object associated with the current app window.

## -parameters

### -param appWindow [in]

A handle to the current window.

### -param riid [iid_is] [in, retval]

 Reference to the identifier of the interface describing the type of interface pointer to return in <i>result</i>.

### -param result

The protection policy manager object for the current window.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/efswrtinterop/nn-efswrtinterop-iprotectionpolicymanagerinterop">IProtectionPolicyManagerInterop</a>