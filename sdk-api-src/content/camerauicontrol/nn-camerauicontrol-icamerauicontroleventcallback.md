---
UID: NN:camerauicontrol.ICameraUIControlEventCallback
title: ICameraUIControlEventCallback
author: windows-sdk-content
description: Callback interface for receiving events from the camera user interface control.
old-location: winprog\icamerauicontroleventcallback.htm
old-project: DevNotes
ms.assetid: f870557e-0e01-4f5c-81be-c709e397e5fd
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ICameraUIControlEventCallback, ICameraUIControlEventCallback interface [Windows API], ICameraUIControlEventCallback interface [Windows API],described, camerauicontrol/ICameraUIControlEventCallback, winprog.icamerauicontroleventcallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: camerauicontrol.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CameraUIControl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CALLFRAME_MARSHALCONTEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - camerauicontrol.h
api_name:
 - ICameraUIControlEventCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICameraUIControlEventCallback interface


## -description


Callback interface for receiving events from the camera user interface control.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICameraUIControlEventCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICameraUIControlEventCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICameraUIControlEventCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d9237bc-38bb-4c14-8485-edec7c739150">OnClosed</a>
</td>
<td align="left" width="63%">
Occurs when the camera UI control is closed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f202b68-48e2-4ae7-ade6-2180c05eec4a">OnItemCaptured</a>
</td>
<td align="left" width="63%">
Occurs when an item is captured.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/008bac9d-4daa-4729-b414-b9551eb636f1">OnItemDeleted</a>
</td>
<td align="left" width="63%">
Occurs when an item is deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/beb50d34-ff68-43e6-8deb-b1ba2c02d70d">OnStartupComplete</a>
</td>
<td align="left" width="63%">
Occurs when startup for the camera UI control has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ec41f09-8278-48ad-838f-9f796617a683">OnSuspendComplete</a>
</td>
<td align="left" width="63%">
Occurs when the camera UI control has completed being suspended.

</td>
</tr>
</table> 

