---
UID: NN:shobjidl.IDynamicHWHandler
title: IDynamicHWHandler
author: windows-sdk-content
description: Called by AutoPlay. Exposes methods that get dynamic information regarding a registered handler prior to displaying it to the user.
old-location: shell\IDynamicHWHandler.htm
old-project: shell
ms.assetid: 924a765f-76b2-4a45-8dc5-74b5e75b437d
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IDynamicHWHandler, IDynamicHWHandler interface [Windows Shell], IDynamicHWHandler interface [Windows Shell],described, _shell_IDynamicHWHandler, shell.IDynamicHWHandler, shobjidl/IDynamicHWHandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shobjidl.h
api_name:
-	IDynamicHWHandler
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# IDynamicHWHandler interface


## -description


Called by AutoPlay. Exposes methods that get dynamic information regarding a registered handler prior to displaying it to the user.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDynamicHWHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDynamicHWHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDynamicHWHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4477600b-311e-4425-b1de-9ed9c396fbdb">GetDynamicInfo</a>
</td>
<td align="left" width="63%">
Called by the system to determine whether a particular handler will be shown before the AutoPlay dialog is displayed.

</td>
</tr>
</table> 


## -remarks



Prior to this interface, when an application registered a handler and was displayed in the autoplay prompt, the handler was always shown as long as the content type (for example, mp3 or avi) associated with that handler was found on the media device. The same icon and action string were always displayed.

If a handler implements this interface prior to showing the handler,  AutoPlay will first call <a href="https://msdn.microsoft.com/4477600b-311e-4425-b1de-9ed9c396fbdb">IDynamicHWHandler::GetDynamicInfo</a> to determine if this handler is to be presented to the user. If you want to show the handler, you may specify a different action string than the one supplied by the static handler registration under <b>HKLM</b>.



