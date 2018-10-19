---
UID: NF:msctf.IEnumTfDisplayAttributeInfo.Next
title: IEnumTfDisplayAttributeInfo::Next
author: windows-sdk-content
description: IEnumTfDisplayAttributeInfo::Next method
old-location: tsf\ienumtfdisplayattributeinfo_next.htm
tech.root: TSF
ms.assetid: db374ba3-8a65-4933-85cb-320c294d6041
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IEnumTfDisplayAttributeInfo interface [Text Services Framework],Next method, IEnumTfDisplayAttributeInfo.Next, IEnumTfDisplayAttributeInfo::Next, Next, Next method [Text Services Framework], Next method [Text Services Framework],IEnumTfDisplayAttributeInfo interface, _tsf_ienumtfdisplayattributeinfo_next_ref, msctf/IEnumTfDisplayAttributeInfo::Next, tsf.ienumtfdisplayattributeinfo_next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IEnumTfDisplayAttributeInfo.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumTfDisplayAttributeInfo::Next


## -description




## -parameters




### -param ulCount [in]

Specifies the number of elements to obtain.


### -param rgInfo [out]

Pointer to an array of <a href="https://msdn.microsoft.com/7f590ecf-06e9-42da-ba40-4364296ae594">ITfDisplayAttributeInfo</a> interface pointers that receives the requested objects. This array must be at least <i>ulCount</i> elements in size.


### -param pcFetched [out]

Pointer to a ULONG value that receives the number of elements actually obtained. The number of elements can be less than the number of items requested. This parameter can be <b>NULL</b>.


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
The method reached the end of the enumeration before the specified number of elements were obtained.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b222deb8-22dd-44c3-9ecc-0fb379682796">IEnumTfDisplayAttributeInfo</a>



<a href="https://msdn.microsoft.com/7f590ecf-06e9-42da-ba40-4364296ae594">ITfDisplayAttributeInfo
      </a>
 

 

