---
UID: NN:tapi3if.IEnumCall
title: IEnumCall
author: windows-sdk-content
description: The IEnumCall interface provides COM-standard enumeration methods for the ITCallInfo interface. The ITCallHub::EnumerateCalls and ITAddress::EnumerateCalls methods return a pointer to IEnumCall.
old-location: tapi3\ienumcall.htm
tech.root: tapi
ms.assetid: 418c1005-98f0-406f-a85c-c08adb269b9f
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: IEnumCall, IEnumCall interface [TAPI 2.2], IEnumCall interface [TAPI 2.2],described, _tapi3_ienumcall, tapi3.ienumcall, tapi3if/IEnumCall
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - IEnumCall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumCall interface


## -description


The 
<b>IEnumCall</b> interface provides COM-standard enumeration methods for the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface. The 
<a href="https://msdn.microsoft.com/becacf70-0ae7-419c-a53f-c6172278d29f">ITCallHub::EnumerateCalls</a> and 
<a href="https://msdn.microsoft.com/2ffa90bf-3005-4fd0-b52f-b155c8b2194f">ITAddress::EnumerateCalls</a> methods return a pointer to 
<b>IEnumCall</b>.

The 
<b>IEnumCall</b> interface is hidden from Visual Basic and scripting languages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumCall</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumCall</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumCall</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/738ee6c6-f287-4c20-a179-6950e7af5591">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5cb911fc-59aa-49c1-9df2-594b0dc22414">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9aa41bab-c575-440b-b1ff-bdbdde68da36">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a60a56cb-3560-4a5a-bdc2-5e578b02ce20">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>
 

 

