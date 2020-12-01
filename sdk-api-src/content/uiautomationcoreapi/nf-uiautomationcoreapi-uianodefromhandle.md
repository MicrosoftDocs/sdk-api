---
UID: NF:uiautomationcoreapi.UiaNodeFromHandle
title: UiaNodeFromHandle function (uiautomationcoreapi.h)
description: Retrieves the UI Automation node associated with a window.
helpviewer_keywords: ["UiaNodeFromHandle","UiaNodeFromHandle function [Windows Accessibility]","uiauto.uiauto_UiaNodeFromHandleFunction","uiauto_UiaNodeFromHandleFunction","uiautomationcoreapi/UiaNodeFromHandle","winauto.uiauto_UiaNodeFromHandleFunction"]
old-location: winauto\uiauto_UiaNodeFromHandleFunction.htm
tech.root: WinAuto
ms.assetid: 0a8c79e6-b825-40a1-b174-5428ab643514
ms.date: 12/05/2018
ms.keywords: UiaNodeFromHandle, UiaNodeFromHandle function [Windows Accessibility], uiauto.uiauto_UiaNodeFromHandleFunction, uiauto_UiaNodeFromHandleFunction, uiautomationcoreapi/UiaNodeFromHandle, winauto.uiauto_UiaNodeFromHandleFunction
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UiaNodeFromHandle
 - uiautomationcoreapi/UiaNodeFromHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - UiaNodeFromHandle
---

# UiaNodeFromHandle function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Retrieves the UI Automation node associated with a window.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The handle of the window.

### -param phnode [out]

Type: <b>HUIANODE*</b>

The address of a variable that receives the handle of the node.
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.