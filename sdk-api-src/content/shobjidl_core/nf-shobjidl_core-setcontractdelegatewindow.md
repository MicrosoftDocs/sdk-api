---
UID: NF:shobjidl_core.SetContractDelegateWindow
title: SetContractDelegateWindow function (shobjidl_core.h)
description: Associates an app window other than the primary foreground window with an app's contracts. Use this function if you are a developer writing a Windows Store app in native C++.
helpviewer_keywords: ["SetContractDelegateWindow","SetContractDelegateWindow function [Windows Shell]","shell.SetContractDelegateWindow","shobjidl_core/SetContractDelegateWindow"]
old-location: shell\SetContractDelegateWindow.htm
tech.root: shell
ms.assetid: 681B2BEC-87C7-40F8-8795-B7965C3FBCCE
ms.date: 12/05/2018
ms.keywords: SetContractDelegateWindow, SetContractDelegateWindow function [Windows Shell], shell.SetContractDelegateWindow, shobjidl_core/SetContractDelegateWindow
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - SetContractDelegateWindow
 - shobjidl_core/SetContractDelegateWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - SetContractDelegateWindow
---

# SetContractDelegateWindow function


## -description

Associates an app window other than the primary foreground window with an app's contracts. Use this function if you are a developer writing a Windows Store app in native C++.

## -parameters

### -param hwndSource [in]

Type: <b>HWND</b>

The handle of the app window normally associated with its contracts.

### -param hwndDelegate [in, optional]

Type: <b>HWND</b>

The handle of another of the app's windows that will act as the contract delegate for <i>hwndSource</i>. Set this value to <b>NULL</b> to remove the delegate connection.

## -remarks

This is an inline function, with the source code included in the header file. It is not included in a .lib or .dll file.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/jj152005(v=vs.85)">GetContractDelegateWindow</a>