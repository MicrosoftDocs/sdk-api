---
UID: NN:shobjidl_core.IInputObjectSite
title: IInputObjectSite
author: windows-sdk-content
description: Exposes a method that is used to communicate focus changes for a user input object contained in the Shell.
old-location: shell\IInputObjectSite.htm
old-project: shell
ms.assetid: fda52080-4117-47d6-8248-ffedd35e7625
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IInputObjectSite, IInputObjectSite interface [Windows Shell], IInputObjectSite interface [Windows Shell],described, _win32_IInputObjectSite, shell.IInputObjectSite, shobjidl_core/IInputObjectSite
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - COM
api_location:
 - Shell32.dll
api_name:
 - IInputObjectSite
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IInputObjectSite interface


## -description


Exposes a method that is used to communicate focus changes for a user input object contained in the Shell.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInputObjectSite</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInputObjectSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInputObjectSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b779beea-534b-4cf0-9426-db2bbcb52277">OnFocusChangeIS</a>
</td>
<td align="left" width="63%">
Informs the browser that the focus has changed.

</td>
</tr>
</table> 


## -remarks



You do not typically implement this interface. <b>IInputObjectSite</b> is implemented by the Shell or the browser to properly maintain the input focus.

You use <b>IInputObjectSite</b> if you are implementing a Shell object that takes user input.

<b>IInputObjectSite</b> is derived from <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>. The listed method is specific to <b>IInputObjectSite</b>.



