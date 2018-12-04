---
UID: NN:msctf.ITfComposition
title: ITfComposition
author: windows-sdk-content
description: The ITfComposition interface is implemented by the TSF manager and is used by a text service to obtain data about and terminate a composition. An instance of this interface is provided by the ITfContextComposition::StartComposition method.
old-location: tsf\itfcomposition.htm
tech.root: TSF
ms.assetid: b1eb5782-13e3-4cbb-8c37-ce7219d1e838
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ITfComposition, ITfComposition interface [Text Services Framework], ITfComposition interface [Text Services Framework],described, _tsf_itfcomposition_ref, msctf/ITfComposition, tsf.itfcomposition
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
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfComposition
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfComposition interface


## -description


The <b>ITfComposition</b> interface is implemented by the TSF manager and is used by a text service to obtain data about and terminate a <a href="https://msdn.microsoft.com/3d9da4f2-ceb9-4abc-8979-d3756d948a57">composition</a>. An instance of this interface is provided by the <a href="https://msdn.microsoft.com/aab84e6c-39c7-438e-b4f0-1d174473aa02">ITfContextComposition::StartComposition</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfComposition</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfComposition</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfComposition</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5717c03-2611-4199-b07d-b6f3b6f65d3a">EndComposition</a>
</td>
<td align="left" width="63%">
Terminates a composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14a726c3-6531-4d49-9f22-20460be02b81">GetRange</a>
</td>
<td align="left" width="63%">
Obtains a range object that contains the text covered by the composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40472318-85de-4cff-ac60-adfcbacc1537">ShiftEnd</a>
</td>
<td align="left" width="63%">
Moves the end anchor of a composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85a5121a-7be0-4703-a1d4-4de21dd98697">ShiftStart</a>
</td>
<td align="left" width="63%">
Moves the start anchor of a composition.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3d9da4f2-ceb9-4abc-8979-d3756d948a57">Compositions</a>



<a href="https://msdn.microsoft.com/aab84e6c-39c7-438e-b4f0-1d174473aa02">ITfContextComposition::StartComposition
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

