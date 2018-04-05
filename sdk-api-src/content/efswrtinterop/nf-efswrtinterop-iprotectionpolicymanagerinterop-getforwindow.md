---
UID: NF:efswrtinterop.IProtectionPolicyManagerInterop.GetForWindow
title: IProtectionPolicyManagerInterop::GetForWindow method
author: windows-driver-content
description: Returns the protection policy manager object associated with the current app window.
old-location: edp\iprotectionpolicymanager_getforwindow.htm
old-project: EDP
ms.assetid: 638316E0-8D5C-4966-A44F-8F31ECBE83EB
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: EDP.iprotectionpolicymanager_getforwindow, GetForWindow method, GetForWindow method, IProtectionPolicyManager interface, GetForWindow,IProtectionPolicyManagerInterop.GetForWindow, IProtectionPolicyManager interface, GetForWindow method, IProtectionPolicyManager::GetForWindow, IProtectionPolicyManagerInterop, IProtectionPolicyManagerInterop::GetForWindow, efswrtinterop/IProtectionPolicyManager::GetForWindow
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
req.typenames: TimedLevel
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	efswrt.dll
api_name:
-	IProtectionPolicyManager.GetForWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: Efswrt.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IProtectionPolicyManagerInterop::GetForWindow method


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




<a href="edp.iprotectionpolicymanager">IProtectionPolicyManager</a>
 

 

