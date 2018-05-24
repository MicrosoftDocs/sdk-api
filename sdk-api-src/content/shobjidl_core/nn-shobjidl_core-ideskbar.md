---
UID: NN:shobjidl_core.IDeskBar
title: IDeskBar
author: windows-driver-content
description: Exposes methods that enable desk bar manipulation.
old-location: shell\IDeskBar.htm
old-project: shell
ms.assetid: 78b9666b-f913-4745-975e-f8dd6e9f89b4
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IDeskBar, IDeskBar interface [Windows Shell], IDeskBar interface [Windows Shell],described, _win32_IDeskBar, shell.IDeskBar, shobjidl_core/IDeskBar
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IDeskBar
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IDeskBar interface


## -description


<p class="CCE_Message">[This interface is supported through Windows XPService Pack 2 (SP2) and Windows Server 2003. It might be unsupported in subsequent versions of Windows.]

Exposes methods that enable desk bar manipulation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDeskBar</b> interface inherits from <a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a>. <b>IDeskBar</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDeskBar</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/003b400c-03a4-47c0-a6b8-04aa65ac573c">GetClient</a>
</td>
<td align="left" width="63%">
Gets the client object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a66093e1-4b91-4edd-abee-0043b437a5f6">OnPosRectChangeDB</a>
</td>
<td align="left" width="63%">
Notifies the object that the rectangle has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26655738-a2d5-446c-af7f-866b34beb3ab">SetClient</a>
</td>
<td align="left" width="63%">
Sets the client specified by <i>punkClient</i>.

</td>
</tr>
</table> 

