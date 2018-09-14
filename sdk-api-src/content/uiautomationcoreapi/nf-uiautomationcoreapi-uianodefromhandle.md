---
UID: NF:uiautomationcoreapi.UiaNodeFromHandle
title: UiaNodeFromHandle function
author: windows-sdk-content
description: Retrieves the UI Automation node associated with a window.
old-location: winauto\uiauto_UiaNodeFromHandleFunction.htm
tech.root: WinAuto
ms.assetid: 0a8c79e6-b825-40a1-b174-5428ab643514
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: UiaNodeFromHandle, UiaNodeFromHandle function [Windows Accessibility], uiauto.uiauto_UiaNodeFromHandleFunction, uiauto_UiaNodeFromHandleFunction, uiautomationcoreapi/UiaNodeFromHandle, winauto.uiauto_UiaNodeFromHandleFunction
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - UiaNodeFromHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaNodeFromHandle function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Retrieves the UI Automation node associated with a window.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The handle of the window.


### -param phnode [out]

Type: <b>HUIANODE*</b>

The address of a variable that receives the handle of the node.
				This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



