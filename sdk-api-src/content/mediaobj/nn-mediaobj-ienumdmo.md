---
UID: NN:mediaobj.IEnumDMO
title: IEnumDMO
author: windows-sdk-content
description: The IEnumDMO interface provides methods for enumerating Microsoft DirectX Media Objects (DMOs). It is based on the OLE enumeration interfaces. For more information, see the IEnumXXXX topic in the Platform SDK.
old-location: dshow\ienumdmo.htm
tech.root: DirectShow
ms.assetid: 221248f2-5c8f-442e-a6ad-e0372ddc1aae
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumDMO, IEnumDMO interface [DirectShow], IEnumDMO interface [DirectShow],described, IEnumDMOInterface, dshow.ienumdmo, mediaobj/IEnumDMO
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mediaobj.h
req.include-header: Dmo.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IEnumDMO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumDMO interface


## -description



The <code>IEnumDMO</code> interface provides methods for enumerating Microsoft DirectX Media Objects (DMOs). It is based on the OLE enumeration interfaces. For more information, see the <i>IEnumXXXX</i> topic in the Platform SDK.



To enumerate registered DMOs, call the <a href="https://msdn.microsoft.com/2cb69d28-15be-44fb-a180-98b560848c08">DMOEnum</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumDMO</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumDMO</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumDMO</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9edca502-7dff-493f-8bce-4bffe8233487">Clone</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5094f2d3-caa7-4085-aebe-306a7b05b591">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a910c70-7f41-43d5-a677-c299b5181638">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32722190-52b5-468a-91d6-a828ad02b203">Skip</a>
</td>
<td align="left" width="63%">
Skips over a specified number of items in the enumeration sequence.

</td>
</tr>
</table> 

