---
UID: NN:shobjidl.IShellView3
title: IShellView3
author: windows-sdk-content
description: Extends the capabilities of IShellView2 by providing a method to replace IShellView2::CreateViewWindow2.
old-location: shell\IShellView3.htm
tech.root: shell
ms.assetid: 96b61e84-0d31-494d-a922-cd3dcd5735b9
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IShellView3, IShellView3 interface [Windows Shell], IShellView3 interface [Windows Shell],described, _shell_IShellView3, shell.IShellView3, shobjidl/IShellView3
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IShellView3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellView3 interface


## -description


Extends the capabilities of <a href="https://msdn.microsoft.com/a61aec39-406d-4066-941d-e788d64f4310">IShellView2</a> by providing a method to replace <a href="https://msdn.microsoft.com/3b829f5f-26ea-4987-be05-6725eeff5fed">IShellView2::CreateViewWindow2</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellView3</b> interface inherits from <a href="https://msdn.microsoft.com/a61aec39-406d-4066-941d-e788d64f4310">IShellView2</a>. <b>IShellView3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellView3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5790f31-922d-41cc-b9a7-0b809615ef1f">CreateViewWindow3</a>
</td>
<td align="left" width="63%">
Requests the creation of a new Shell view window. The view can be either the right pane of Windows Explorer or the client window of a folder window. This method replaces <a href="https://msdn.microsoft.com/3b829f5f-26ea-4987-be05-6725eeff5fed">IShellView2::CreateViewWindow2</a>.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> and <a href="https://msdn.microsoft.com/a61aec39-406d-4066-941d-e788d64f4310">IShellView2</a> interfaces, from which it inherits.



