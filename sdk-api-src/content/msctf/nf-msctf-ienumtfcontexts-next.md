---
UID: NF:msctf.IEnumTfContexts.Next
title: IEnumTfContexts::Next
author: windows-driver-content
description: IEnumTfContexts::Next method
old-location: tsf\ienumtfcontexts_next.htm
old-project: TSF
ms.assetid: 0727ae8b-a66f-42a7-bc74-4c01bfff3855
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IEnumTfContexts interface [Text Services Framework],Next method, IEnumTfContexts.Next, IEnumTfContexts::Next, Next, Next method [Text Services Framework], Next method [Text Services Framework],IEnumTfContexts interface, _tsf_ienumtfcontexts_next_ref, msctf/IEnumTfContexts::Next, tsf.ienumtfcontexts_next
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
-	msctf.dll
api_name:
-	IEnumTfContexts.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# IEnumTfContexts::Next


## -description




## -parameters




### -param ulCount [in]

Specifies the number of elements to obtain.


### -param rgContext [out]

Pointer to an array of <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a> interface pointers that receives the requested objects. This array must be at least <i>ulCount</i> elements in size.


### -param pcFetched [out]

Pointer to a ULONG value that receives the number of elements actually obtained. This value can be less than the number of items requested. This parameter can be <b>NULL</b>.


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
<i>rgContext</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/20b342e6-cac4-4bc5-820b-e397e0ce4648">IEnumTfContexts</a>



<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>
 

 

