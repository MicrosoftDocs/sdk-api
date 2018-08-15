---
UID: NN:vss.IVssEnumObject
title: IVssEnumObject
author: windows-sdk-content
description: Contains methods to iterate over and perform other operations on a list of enumerated objects.
old-location: base\ivssenumobject.htm
old-project: vss
ms.assetid: b8e80909-a28a-45d7-87e2-4f44bf6990f4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IVssEnumObject, IVssEnumObject interface [VSS], IVssEnumObject interface [VSS],described, _win32_ivssenumobject, base.ivssenumobject, vss/IVssEnumObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vss.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VSS_WRITER_STATE, *PVSS_WRITER_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssEnumObject
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssEnumObject interface


## -description


The <b>IVssEnumObject</b> interface contains methods 
    to iterate over and perform other operations on a list of enumerated objects.

The calling application is responsible for calling 
    <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> to release the resources held by the 
    returned <b>IVssEnumObject</b> when it is no longer needed. It 
    may also need to call <b>IUnknown::Release</b> to release 
    temporary objects (such as strings) returned during enumeration.

The <a href="https://msdn.microsoft.com/3f79bf84-c7b9-4291-ae3b-7061fe3199e9">IVssBackupComponents::Query</a> method 
    returns an <b>IVssEnumObject</b> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssEnumObject</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVssEnumObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssEnumObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71bf3789-247e-4e3f-8200-a4309a7c2d8c">Clone</a>
</td>
<td align="left" width="63%">
Copies the specified list of enumerated objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bfaba94-802f-47f5-9843-acc05b32f1b2">Next</a>
</td>
<td align="left" width="63%">
Returns the next specified number of objects from the list of enumerated objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98fc07b0-3efe-4ec3-bb70-64a8b8828162">Reset</a>
</td>
<td align="left" width="63%">
Clears the list of enumerated objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a655978e-49fa-445d-8576-ba82b523750c">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of objects in the list of enumerated objects.

</td>
</tr>
</table> 

