---
UID: NN:wsbapp.IWsbApplicationRestoreSupport
title: IWsbApplicationRestoreSupport
author: windows-sdk-content
description: Defines methods for performing application-specific restore tasks.
old-location: wsb\iwsbapplicationrestoresupport.htm
old-project: wsb
ms.assetid: 694f9b4d-0ca8-4dbe-829c-6ac18c9aa140
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWsbApplicationRestoreSupport, IWsbApplicationRestoreSupport interface [Windows Server Backup], IWsbApplicationRestoreSupport interface [Windows Server Backup],described, wsb.iwsbapplicationrestoresupport, wsbapp/IWsbApplicationRestoreSupport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wsbapp.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsbApp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSPUPCALLTABLE, *LPWSPUPCALLTABLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WsbApp.h
api_name:
 - IWsbApplicationRestoreSupport
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWsbApplicationRestoreSupport interface


## -description


Defines methods for performing application-specific restore tasks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWsbApplicationRestoreSupport</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWsbApplicationRestoreSupport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWsbApplicationRestoreSupport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6dae61b7-0e52-42f7-8ca4-b3566f6b4bbc">IsRollForwardSupported</a>
</td>
<td align="left" width="63%">
Reports whether the application supports roll-forward restore.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15250479-841d-421e-8780-6dee795f29b5">OrderComponents</a>
</td>
<td align="left" width="63%">
Specifies the order in which application components are to be restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8be7975e-9b94-4a6e-b1f5-794b8749ccbe">PostRestore</a>
</td>
<td align="left" width="63%">
Performs application-specific <a href="https://msdn.microsoft.com/44279c0e-17f4-4109-bc12-af9064cd321e">PostRestore</a> operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e1b73f9-a931-42a2-a1b1-f939f492c449">PreRestore</a>
</td>
<td align="left" width="63%">
Performs application-specific <a href="https://msdn.microsoft.com/44279c0e-17f4-4109-bc12-af9064cd321e">PreRestore</a> operations.

</td>
</tr>
</table> 

