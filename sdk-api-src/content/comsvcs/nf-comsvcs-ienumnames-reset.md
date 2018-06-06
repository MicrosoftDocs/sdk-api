---
UID: NF:comsvcs.IEnumNames.Reset
title: IEnumNames::Reset
author: windows-sdk-content
description: Resets the enumeration sequence to the beginning.
old-location: cos\ienumnames_reset.htm
old-project: cossdk
ms.assetid: e7b7e703-f5d5-430f-8fa6-c26a236eab88
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IEnumNames interface [COM+],Reset method, IEnumNames.Reset, IEnumNames::Reset, Reset, Reset method [COM+], Reset method [COM+],IEnumNames interface, _cos_IEnumNames_Reset, comsvcs/IEnumNames::Reset, cos.ienumnames_reset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IEnumNames.Reset
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IEnumNames::Reset


## -description


Resets the enumeration sequence to the beginning.


## -parameters






## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The enumeration sequence was reset.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The enumeration sequence was reset, but there are no items in the enumerator.

</td>
</tr>
</table>
 




## -remarks



You can use the S_FALSE return value as an optimization to detect an empty enumeration.

A call to this method, resetting the sequence, does not guarantee that the same set of objects will be enumerated after the reset, because the collection may have changed.




## -see-also




<a href="https://msdn.microsoft.com/9f70b554-3cdd-4a4b-b180-c6de6182a46a">IEnumNames</a>
 

 

