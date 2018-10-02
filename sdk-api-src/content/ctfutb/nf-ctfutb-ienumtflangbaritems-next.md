---
UID: NF:ctfutb.IEnumTfLangBarItems.Next
title: IEnumTfLangBarItems::Next
author: windows-sdk-content
description: IEnumTfLangBarItems::Next method
old-location: tsf\ienumtflangbaritems_next.htm
tech.root: TSF
ms.assetid: 46e24685-581c-4c68-80df-4465e90e3e36
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IEnumTfLangBarItems interface [Text Services Framework],Next method, IEnumTfLangBarItems.Next, IEnumTfLangBarItems::Next, Next, Next method [Text Services Framework], Next method [Text Services Framework],IEnumTfLangBarItems interface, _tsf_ienumtflangbaritems_next_ref, ctfutb/IEnumTfLangBarItems::Next, tsf.ienumtflangbaritems_next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
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
 - IEnumTfLangBarItems.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumTfLangBarItems::Next


## -description




## -parameters




### -param ulCount [in]

Specifies the number of elements to obtain.


### -param ppItem [out]

Pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/ms628701(v=VS.85).aspx">ITfLangBarItem</a> interface pointers that receives the requested objects. This array must be at least <i>ulCount</i> elements in size.


### -param pcFetched

[in, out] Pointer to a ULONG value that receives the number of elements obtained. This value can be less than the number of items requested. This parameter can be <b>NULL</b>.


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
<i>ppItem</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms538185(v=VS.85).aspx">IEnumTfLangBarItems</a>



<a href="https://msdn.microsoft.com/16612641-2bff-4e6f-a955-85793021a20b">ITfLangBarItem
      </a>
 

 

