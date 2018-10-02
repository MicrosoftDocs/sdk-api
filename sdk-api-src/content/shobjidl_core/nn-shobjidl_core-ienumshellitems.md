---
UID: NN:shobjidl_core.IEnumShellItems
title: IEnumShellItems
author: windows-sdk-content
description: Exposes enumeration of IShellItem interfaces. This interface is typically obtained by calling the IEnumShellItems method.
old-location: shell\IEnumShellItems.htm
tech.root: Shell
ms.assetid: 07aed597-359f-4f4b-9edf-168c15bdc58e
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IEnumShellItems, IEnumShellItems interface [Windows Shell], IEnumShellItems interface [Windows Shell],described, _shell_IEnumShellItems, shell.IEnumShellItems, shobjidl_core/IEnumShellItems
ms.prod: windows
ms.technology: windows-sdk
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
 - IEnumShellItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumShellItems interface


## -description


Exposes enumeration of <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> interfaces. This interface is typically obtained by calling the <b>IEnumShellItems</b> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumShellItems</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumShellItems</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumShellItems</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccfe8ab0-8bc5-4270-9189-01bac38ce36a">Clone</a>
</td>
<td align="left" width="63%">
Gets a copy of the current enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8074ecea-30b9-4d1e-9184-457d3dd70bb8">Next</a>
</td>
<td align="left" width="63%">
Gets an array of one or more <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> interfaces from the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0208a68-0513-4fa9-88ae-2147cf61bcb5">Reset</a>
</td>
<td align="left" width="63%">
Resets the internal count of retrieved <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> interfaces in the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5359c9d2-715a-4949-8f40-a35d04423dba">Skip</a>
</td>
<td align="left" width="63%">
Skips a given number of <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> interfaces in the enumeration. Used when retrieving interfaces.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>
 

 

