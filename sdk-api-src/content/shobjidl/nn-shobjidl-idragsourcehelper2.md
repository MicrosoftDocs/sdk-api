---
UID: NN:shobjidl.IDragSourceHelper2
title: IDragSourceHelper2
author: windows-sdk-content
description: Exposes a method that adds functionality to IDragSourceHelper. This method sets the characteristics of a drag-and-drop operation over an IDragSourceHelper object.
old-location: shell\IDragSourceHelper2.htm
old-project: shell
ms.assetid: 20529b27-22d2-4c77-a2a7-93e54b0b7748
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDragSourceHelper2, IDragSourceHelper2 interface [Windows Shell], IDragSourceHelper2 interface [Windows Shell],described, _shell_IDragSourceHelper2, shell.IDragSourceHelper2, shobjidl/IDragSourceHelper2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
req.redist: 
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
 - Shell32.dll
api_name:
 - IDragSourceHelper2
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# IDragSourceHelper2 interface


## -description


Exposes a method that adds functionality to <a href="https://msdn.microsoft.com/d68ac8fd-4d9c-47ee-bdff-0c5bae6b5e28">IDragSourceHelper</a>. This method sets the characteristics of a drag-and-drop operation over an <b>IDragSourceHelper</b> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDragSourceHelper2</b> interface inherits from <a href="https://msdn.microsoft.com/d68ac8fd-4d9c-47ee-bdff-0c5bae6b5e28">IDragSourceHelper</a>. <b>IDragSourceHelper2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDragSourceHelper2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fe9b753-5ac1-4b6f-9538-5259870404ec">SetFlags</a>
</td>
<td align="left" width="63%">
Sets the characteristics of a drag-and-drop operation over an <a href="https://msdn.microsoft.com/d68ac8fd-4d9c-47ee-bdff-0c5bae6b5e28">IDragSourceHelper</a> object.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/d68ac8fd-4d9c-47ee-bdff-0c5bae6b5e28">IDragSourceHelper</a> interface, from which it inherits.

If you want to adjust the behavior of the drag image by calling <a href="https://msdn.microsoft.com/1fe9b753-5ac1-4b6f-9538-5259870404ec">IDragSourceHelper2::SetFlags</a>, that call should be made before you call <a href="https://msdn.microsoft.com/0bcdfe92-cec0-44f3-a345-5b560d52fae9">InitializeFromWindow</a> or <a href="https://msdn.microsoft.com/d50be9c9-f407-4386-bb8f-04c849205359">InitializeFromBitmap</a>.



