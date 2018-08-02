---
UID: NF:uiautomationcoreapi.UiaReturnRawElementProvider
title: UiaReturnRawElementProvider function
author: windows-sdk-content
description: Gets an interface to the UI Automation provider for a window.
old-location: winauto\uiauto_UiaReturnRawElementProviderFunction.htm
old-project: WinAuto
ms.assetid: 800dfad2-2263-4069-a1fe-f737842b3357
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: UiaReturnRawElementProvider, UiaReturnRawElementProvider function [Windows Accessibility], uiauto.uiauto_UiaReturnRawElementProviderFunction, uiauto_UiaReturnRawElementProviderFunction, uiautomationcoreapi/UiaReturnRawElementProvider, winauto.uiauto_UiaReturnRawElementProviderFunction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
 - Ext-MS-Win-uiacore-l1-1-0.dll
 - Ext-MS-Win-UIaCore-l1-1-1.dll
 - Ext-MS-Win-UIaCore-l1-1-2.dll
 - Ext-MS-Win-UiaCore-L1-1-3.dll
api_name:
 - UiaReturnRawElementProvider
product: Windows
targetos: Windows
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# UiaReturnRawElementProvider function


## -description


Gets an interface to the UI Automation provider for a window.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The handle of the window containing the element served by the provider.


### -param wParam

TBD


### -param lParam

TBD


### -param el [in]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>*</b>

The UI Automation provider.


#### - lparam [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

The <i>lParam</i> argument of the <a href="https://msdn.microsoft.com/59350aa1-1697-4110-b9a6-f30ee56c4cff">WM_GETOBJECT</a> message. 


#### - wparam [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WPARAM</a></b>

The <i>wParam</i> argument of the <a href="https://msdn.microsoft.com/59350aa1-1697-4110-b9a6-f30ee56c4cff">WM_GETOBJECT</a> message.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LRESULT</a></b>

The key for the client process to connect to the server process through UI Automation.

This function returns zero when it is used to notify UI Automation that it is safe to remove the provider raised-event map. For more information, see Remarks.




## -remarks



This function is called by a control when it receives the <a href="https://msdn.microsoft.com/59350aa1-1697-4110-b9a6-f30ee56c4cff">WM_GETOBJECT</a> message, to provide UI Automation with the UI Automation provider for the control. The control should pass the <i>wParam</i> and <i>lParam</i> parameters to the <b>UiaReturnRawElementProvider</b> function without filtering them first, because filtering can cause problems with Microsoft Active Accessibility clients. The control's window procedure should return the result of calling <b>UiaReturnRawElementProvider</b>.

When Microsoft Active Accessibility clients are listening to events raised by a UI Automation provider, UI Automation maintains a map of the providers that have raised events. When the Microsoft Active Accessibility clients request further information, UI Automation uses the map to route the requests to the appropriate providers. When a window that previously returned providers has been destroyed, you should notify UI Automation by calling the <b>UiaReturnRawElementProvider</b> function as follows: <code>UiaReturnRawElementProvider(hwnd, 0, 0, NULL)</code>. This call tells UI Automation that it can safely remove all map entries that refer to the specified window. This call can save memory because it releases references to the providers being held by the raised-event map. The function returns zero when called with these special parameters. Microsoft recommends making this call from the <a href="https://msdn.microsoft.com/en-us/library/ms632620(v=VS.85).aspx">WM_DESTROY</a> message handler of the window that returns the UI Automation providers.



