---
UID: NN:shobjidl.IAccessibleObject
title: IAccessibleObject
author: windows-sdk-content
description: Exposes a method that can be used by an accessibility application.
old-location: shell\IAccessibleObject.htm
tech.root: shell
ms.assetid: bac49a2d-4357-4607-a89d-d2ed4abf89bb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAccessibleObject, IAccessibleObject interface [Windows Shell], IAccessibleObject interface [Windows Shell],described, _shell_IAccessibleObject, shell.IAccessibleObject, shobjidl/IAccessibleObject
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
 - IAccessibleObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAccessibleObject interface


## -description


Exposes a method that can be used by an accessibility application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccessibleObject</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAccessibleObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccessibleObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/455d9434-1ea3-4a4e-ae4d-0952c895178c">SetAccessibleName</a>
</td>
<td align="left" width="63%">
Sets text that is retrieved by <a href="https://msdn.microsoft.com/344e95e1-45a5-4951-b545-1a938bfc8a8c">IAccessible::get_accName</a> which accessibility tools use to obtain the Name Property of an object.


</td>
</tr>
</table> 

