---
UID: NN:shobjidl_core.IEnumObjects
title: IEnumObjects
author: windows-sdk-content
description: Exposes methods to enumerate unknown objects.
old-location: shell\IEnumObjects.htm
tech.root: shell
ms.assetid: 914f2a4d-a67a-45d9-96ee-d8cae7d08e3c
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IEnumObjects, IEnumObjects interface [Windows Shell], IEnumObjects interface [Windows Shell],described, _shell_IEnumObjects, shell.IEnumObjects, shobjidl_core/IEnumObjects
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
 - IEnumObjects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumObjects interface


## -description


Exposes methods to enumerate unknown objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumObjects</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumObjects</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumObjects</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17dd1539-cf98-4cbf-8c06-4e21123f6f54">Clone</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c79d3e2-c1c9-4529-9a60-457c2d2e6af5">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number and type of objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/646ffef2-294e-461d-97e4-39cb68bb85df">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration index to 0.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/227be42b-c821-40f4-8bcb-9990d1ceefeb">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of objects.

</td>
</tr>
</table> 

