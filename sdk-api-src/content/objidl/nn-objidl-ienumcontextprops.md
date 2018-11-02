---
UID: NN:objidl.IEnumContextProps
title: IEnumContextProps
author: windows-sdk-content
description: Provides a mechanism for enumerating the context properties associated with a COM+ object context.
old-location: com\ienumcontextprops.htm
tech.root: com
ms.assetid: 64591e45-5478-4360-8c1f-08b09b5aef8e
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IEnumContextProps, IEnumContextProps interface [COM], IEnumContextProps interface [COM],described, _com_ienumcontextprops, com.ienumcontextprops, objidlbase/IEnumContextProps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - objidlbase.h
api_name:
 - IEnumContextProps
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumContextProps interface


## -description


Provides a mechanism for enumerating the context properties associated with a COM+ object context.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumContextProps</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IEnumContextProps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumContextProps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bf7f7da-9e40-49bd-9bd0-d2fcdfc2f517">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad3194f7-0df4-4f26-8a98-2715188fb63f">Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of context properties in the context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1856f5c-dfed-462c-aca3-91b7973d6d8d">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de6a45d2-f0f7-4233-92d2-8e59d4685557">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22c50b48-a6e2-4153-9604-57f07512d4ce">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table> 

