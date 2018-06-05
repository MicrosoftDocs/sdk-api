---
UID: NF:uiautomationcoreapi.UiaGetRuntimeId
title: UiaGetRuntimeId function
author: windows-sdk-content
description: Retrieves the runtime identifier of a UI Automation node.
old-location: winauto\uiauto_UiaGetRuntimeIdAutoMeth.htm
old-project: WinAuto
ms.assetid: 3b339cda-3569-4705-b5cf-028c354d627e
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: UiaGetRuntimeId, UiaGetRuntimeId function [Windows Accessibility], uiauto.uiauto_UiaGetRuntimeIdAutoMeth, uiauto_UiaGetRuntimeIdAutoMeth, uiautomationcoreapi/UiaGetRuntimeId, winauto.uiauto_UiaGetRuntimeIdAutoMeth
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Uiautomationcore.dll
api_name:
-	UiaGetRuntimeId
product: Windows
targetos: Windows
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# UiaGetRuntimeId function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Retrieves the runtime identifier of a UI Automation node.


## -parameters




### -param hnode [in]

Type: <b>HUIANODE</b>

The node for which the identifier is being requested.


### -param pruntimeId [out]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

The address of a variable that receives a pointer to a <a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> that contains the runtime identifier of the type VT_I4. This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.




## -remarks



The runtime identifier should be treated as an opaque value and used only for comparison.



