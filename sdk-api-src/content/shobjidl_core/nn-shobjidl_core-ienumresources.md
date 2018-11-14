---
UID: NN:shobjidl_core.IEnumResources
title: IEnumResources
author: windows-sdk-content
description: Exposes resource enumeration methods.
old-location: shell\IEnumResources.htm
tech.root: shell
ms.assetid: 28c645cf-8c69-49d7-a95f-ced6467ad682
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IEnumResources, IEnumResources interface [Windows Shell], IEnumResources interface [Windows Shell],described, _shell_IEnumResources, shell.IEnumResources, shobjidl_core/IEnumResources
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
 - shobjidl_core.h
api_name:
 - IEnumResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumResources interface


## -description


Exposes resource enumeration methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumResources</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumResources</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumResources</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/660243ba-263d-4f4a-b26f-ab831f60d76b">Clone</a>
</td>
<td align="left" width="63%">
Clones a resource enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5d0d754-4252-476a-b3af-0ba257eab339">Next</a>
</td>
<td align="left" width="63%">
Gets the next <a href="https://msdn.microsoft.com/92ca56a2-e2c3-4651-aa29-115eb07119e9">SHELL_ITEM_RESOURCE</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b3f38d2-80fe-4242-a99d-5d82f9dd50e9">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration index to 0.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3dc94e7-5455-4afb-8743-05c993e1448b">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of resources.

</td>
</tr>
</table> 

