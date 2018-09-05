---
UID: NN:shobjidl_core.IInputObject
title: IInputObject
author: windows-sdk-content
description: Exposes methods that change UI activation and process accelerators for a user input object contained in the Shell.
old-location: shell\IInputObject.htm
old-project: shell
ms.assetid: 5fbbcd26-c60a-4b6a-92cf-36b8bd429266
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IInputObject, IInputObject interface [Windows Shell], IInputObject interface [Windows Shell],described, _win32_IInputObject, shell.IInputObject, shobjidl_core/IInputObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
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
 - COM
api_location:
 - Shell32.dll
api_name:
 - IInputObject
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IInputObject interface


## -description


Exposes methods that change UI activation and process accelerators for a user input object contained in the Shell.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInputObject</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInputObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInputObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f22f6b54-9d71-4451-81bf-6e3fd01ab36a">HasFocusIO</a>
</td>
<td align="left" width="63%">
Determines if one of the object's windows has the keyboard focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e075556a-2910-41ee-a8f3-3fba1cd55a35">TranslateAcceleratorIO</a>
</td>
<td align="left" width="63%">
Enables the object to process keyboard accelerators.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a725863e-4814-4aa7-99c6-7e7141db214d">UIActivateIO</a>
</td>
<td align="left" width="63%">
UI-activates or deactivates the object.

</td>
</tr>
</table> 


## -remarks



Implement <b>IInputObject</b> if you are implementing a Shell object that takes user input.

You do not call this interface directly. <b>IInputObject</b> is used by the Shell or the browser to notify the object of UI activation changes and to translate keyboard accelerators.

<b>IInputObject</b> is derived from <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>. The listed methods are specific to <b>IInputObject</b>.



