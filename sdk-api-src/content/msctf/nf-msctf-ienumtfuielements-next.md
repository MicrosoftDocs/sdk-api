---
UID: NF:msctf.IEnumTfUIElements.Next
title: IEnumTfUIElements::Next method
author: windows-driver-content
description: The IEnumTfUIElements::Next method obtains, from the current position, the specified number of elements in the enumeration sequence.
old-location: tsf\ienumtfuielements_next.htm
old-project: TSF
ms.assetid: ed3cdae9-5626-4967-97b8-51c94ac23963
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IEnumTfUIElements, IEnumTfUIElements interface [Text Services Framework], Next method, IEnumTfUIElements::Next, Next method [Text Services Framework], Next method [Text Services Framework], IEnumTfUIElements interface, Next,IEnumTfUIElements.Next, msctf/IEnumTfUIElements::Next, tsf.ienumtfuielements_next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	IEnumTfUIElements.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# IEnumTfUIElements::Next method


## -description


The <b>IEnumTfUIElements::Next</b> method obtains, from the current position, the specified number of elements in the enumeration sequence.


## -parameters




### -param ulCount [out]

[out] Specifies the number of elements to obtain.


### -param ppElement [out]

[out] Pointer to an array of <a href="https://msdn.microsoft.com/651c3ca1-5e5b-4978-80d2-2183bd158610">ITfUIElement</a> interface pointer. This array must be at least <i>ulCount</i> elements in size.


### -param pcFetched [out]

[out] Pointer to a ULONG value that receives the number of elements actually obtained. This value can be less than the number of items requested. This parameter can be <b>NULL</b>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method reached the end of the enumeration before the specified number of elements could be obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 



