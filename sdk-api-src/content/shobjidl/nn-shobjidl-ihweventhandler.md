---
UID: NN:shobjidl.IHWEventHandler
title: IHWEventHandler
author: windows-sdk-content
description: Called by AutoPlay to implement the handling of registered media types.
old-location: shell\IHWEventHandler.htm
tech.root: shell
ms.assetid: be49322a-99b2-4626-8e9d-29965bbe182d
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: IHWEventHandler, IHWEventHandler interface [Windows Shell], IHWEventHandler interface [Windows Shell],described, inet_IHWEventHandler, shell.IHWEventHandler, shobjidl/IHWEventHandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.5 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IHWEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IHWEventHandler interface


## -description


Called by AutoPlay to implement the handling of registered media types.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IHWEventHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IHWEventHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IHWEventHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/575ca84c-8cf9-4ed6-a997-844cf0533986">HandleEvent</a>
</td>
<td align="left" width="63%">
Handles AutoPlay device events for which there is no content of the type the application is registered to handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5787ebd-2784-4e86-b749-93258a1a26bd">HandleEventWithContent</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96eb582a-4f32-4e13-ad01-8b5ffabab582">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an object that contains an implementation of the <b>IHWEventHandler</b> interface.

</td>
</tr>
</table> 


## -remarks



Developers supporting this interface must expose it in a Component Object Model (COM) server.

All applications registered as AutoPlay media handlers must implement this interface. Handlers that implement this interface should return quickly from calls to <a href="https://msdn.microsoft.com/575ca84c-8cf9-4ed6-a997-844cf0533986">IHWEventHandler::HandleEvent</a> and  <a href="https://msdn.microsoft.com/65720250-ace5-488d-9be7-33b07d7cc667">IHWEventHandler2::HandleEventWithHWND</a> so they won't block the AutoPlay dialog from closing. Additionally, if a local server must be launched for the creation of this handler, it should not block the CreateInstance call; it should return as soon as possible.
      



