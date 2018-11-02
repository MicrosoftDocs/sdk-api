---
UID: NF:uiautomationcoreapi.UiaProviderForNonClient
title: UiaProviderForNonClient function
author: windows-sdk-content
description: Gets the provider for the entire non-client area of a window, or for a control in the non-client area of a window.
old-location: winauto\uiauto_UiaProviderForNonClientFunction.htm
tech.root: WinAuto
ms.assetid: 440E6659-C62F-4567-B00F-B0F0B0F21817
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: UiaProviderForNonClient, UiaProviderForNonClient function [Windows Accessibility], uiautomationcoreapi/UiaProviderForNonClient, winauto.uiauto_UiaProviderForNonClientFunction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - UiaProviderForNonClient
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaProviderForNonClient function


## -description


Gets the provider for the entire non-client area of a window, or  for a control in the  non-client area of a window.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The window that owns the non-client area or non-client control.


### -param idObject [in]

Type: <b>long</b>

The object identifier of the non-client control, or <a href="https://msdn.microsoft.com/en-us/library/Dd373606(v=VS.85).aspx">OBJID_WINDOW</a> for the entire non-client area. For a list of possible values, see <b>Object Identifiers</b>.


### -param idChild [in]

Type: <b>long</b>

The child identifier of the non-client control.


### -param ppProvider [out]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>**</b>

Receives the provider for the non-client area or non-client control.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.




## -remarks



This function returns the default Microsoft UI Automation provider for the non-client area of a window.  UI Automation supports the non-client area without any explicit help from the window. You can override and customize the support by using the <a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a> interface that is retrieved by this function.  

This function is particularly useful when you use it with the <a href="https://msdn.microsoft.com/en-us/library/Ee671599(v=VS.85).aspx">ProviderOptions_RefuseNonClientSupport</a> flag, which disables the UI Automation default provider for the non-client area so that the window can supply  its own provider.



The supported object IDs for controls in the non-client area include <a href="https://msdn.microsoft.com/en-us/library/Dd373606(v=VS.85).aspx">OBJID_WINDOW</a><a href="https://msdn.microsoft.com/en-us/library/Dd373606(v=VS.85).aspx">, OBJID_VSCROLL</a>, <a href="https://msdn.microsoft.com/en-us/library/Dd373606(v=VS.85).aspx">OBJID_HSCROLL</a>, <a href="https://msdn.microsoft.com/en-us/library/Dd373606(v=VS.85).aspx">OBJID_TITLEBAR</a>, <a href="https://msdn.microsoft.com/en-us/library/Dd373606(v=VS.85).aspx">OBJID_MENU</a>, and <a href="https://msdn.microsoft.com/en-us/library/Dd373606(v=VS.85).aspx">OBJID_SIZEGRIP</a>.  For <b>OBJID_TITLEBAR</b>, use the child ID to distinguish between the entire title bar and the buttons that it contains.





## -see-also




<a href="https://msdn.microsoft.com/76012ec7-0114-4b6b-a35e-5cfde5b90230">Functions for Providers</a>
 

 

