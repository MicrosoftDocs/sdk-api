---
UID: NF:efswrtinterop.IProtectionPolicyManagerInterop.GetForWindow
title: IProtectionPolicyManagerInterop::GetForWindow
author: windows-sdk-content
description: Returns the protection policy manager object associated with the current app window.
old-location: edp\iprotectionpolicymanager_getforwindow.htm
tech.root: EDP
ms.assetid: 638316E0-8D5C-4966-A44F-8F31ECBE83EB
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EDP.iprotectionpolicymanager_getforwindow, GetForWindow, GetForWindow method, GetForWindow method,IProtectionPolicyManagerInterop interface, IProtectionPolicyManagerInterop interface,GetForWindow method, IProtectionPolicyManagerInterop.GetForWindow, IProtectionPolicyManagerInterop::GetForWindow, efswrtinterop/IProtectionPolicyManagerInterop::GetForWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - efswrt.dll
api_name:
 - IProtectionPolicyManagerInterop.GetForWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/AFA7F918-8730-40A2-871E-9356391B47F8">IProtectionPolicyManagerInterop</a>
 

 

