---
UID: NF:shobjidl_core.SetContractDelegateWindow
title: SetContractDelegateWindow function
author: windows-sdk-content
description: Associates an app window other than the primary foreground window with an app's contracts. Use this function if you are a developer writing a Windows Store app in native C++.
old-location: shell\SetContractDelegateWindow.htm
tech.root: shell
ms.assetid: 681B2BEC-87C7-40F8-8795-B7965C3FBCCE
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: SetContractDelegateWindow, SetContractDelegateWindow function [Windows Shell], shell.SetContractDelegateWindow, shobjidl_core/SetContractDelegateWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - SetContractDelegateWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


## -returns



This function does not return a value.




## -remarks



This is an inline function, with the source code included in the header file. It is not included in a .lib or .dll file.




## -see-also




<a href="https://msdn.microsoft.com/89B23CB0-50CF-43BE-B397-542FA433018D">GetContractDelegateWindow</a>
 

 

