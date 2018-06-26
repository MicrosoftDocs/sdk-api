---
UID: NN:shobjidl.IStreamAsync
title: IStreamAsync
author: windows-sdk-content
description: Exposes methods to manage input/outpout (I/O) to an asynchronous stream.
old-location: shell\IStreamAsync.htm
old-project: shell
ms.assetid: 2d436312-3d61-4511-9342-711b2f7d4717
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IStreamAsync, IStreamAsync interface [Windows Shell], IStreamAsync interface [Windows Shell],described, _shell_IStreamAsync, shell.IStreamAsync, shobjidl/IStreamAsync
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IStreamAsync
product: Windows
targetos: Windows
req.lib: Comdlg32.lib
req.dll: Shell32.dll (version 6.0.6000 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# IStreamAsync interface


## -description



            Exposes methods to manage input/outpout (I/O) to an asynchronous stream.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamAsync</b> interface inherits from <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>. <b>IStreamAsync</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamAsync</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca2a1c59-b538-4c1b-9ad3-89d00f19325d">CancelIo</a>
</td>
<td align="left" width="63%">
Marks all pending input/output (I/O) operations as canceled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a53934f-bbff-4bb0-b374-01adb629a041">OverlappedResult</a>
</td>
<td align="left" width="63%">
Retrieves the results of an overlapped operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0046a89-1427-465e-a5f3-2398ebff04f3">ReadAsync</a>
</td>
<td align="left" width="63%">
Reads information from a stream asynchronously. For example, the Shell implements this interface on file items when transferring them asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5004923-191b-4ec1-83af-f066209c786a">WriteAsync</a>
</td>
<td align="left" width="63%">
Writes information to a stream asynchronously. For example, the Shell implements this method on file items when transferring them asynchronously.

</td>
</tr>
</table> 

