---
UID: NN:msctf.IEnumTfUIElements
title: IEnumTfUIElements
author: windows-sdk-content
description: The IEnumTfUIElements interface is implemented by TSF manager and used by applications or textservices. This interface can be retrieved by ITfUIElementMgr::EnumUIElements and enumerates the registered UI elements.
old-location: tsf\ienumtfuielements.htm
tech.root: TSF
ms.assetid: 5ee3d89c-0761-4d4b-9fd9-6b9de7ceb077
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumTfUIElements, IEnumTfUIElements interface [Text Services Framework], IEnumTfUIElements interface [Text Services Framework],described, _tsf_ienumtfuielements_ref, msctf/IEnumTfUIElements, tsf.ienumtfuielements
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
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
 - Msctf.h
api_name:
 - IEnumTfUIElements
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumTfUIElements interface


## -description


The <b>IEnumTfUIElements</b> interface is implemented by TSF manager and used by applications or textservices. This interface can be retrieved by <a href="https://msdn.microsoft.com/cdede376-be18-4deb-ae79-594aebb085a6">ITfUIElementMgr::EnumUIElements</a>  and enumerates the registered UI elements.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTfUIElements</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumTfUIElements</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTfUIElements</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3949ea4d-9360-4524-9495-31a884cac309">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed3cdae9-5626-4967-97b8-51c94ac23963">Next</a>
</td>
<td align="left" width="63%">
Obtains, from the current position, the specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a87b067f-251c-47d1-b57a-32e6524adc57">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44ba8fb1-e702-4f53-b95a-719b4fdfcaa0">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table> 

