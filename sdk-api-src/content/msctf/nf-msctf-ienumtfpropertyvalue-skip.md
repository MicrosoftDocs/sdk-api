---
UID: NF:msctf.IEnumTfPropertyValue.Skip
title: IEnumTfPropertyValue::Skip
author: windows-sdk-content
description: IEnumTfPropertyValue::Skip method
old-location: tsf\ienumtfpropertyvalue_skip.htm
old-project: TSF
ms.assetid: 6bc11b63-c8d8-453d-b667-8a087b24cf47
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEnumTfPropertyValue interface [Text Services Framework],Skip method, IEnumTfPropertyValue.Skip, IEnumTfPropertyValue::Skip, Skip, Skip method [Text Services Framework], Skip method [Text Services Framework],IEnumTfPropertyValue interface, _tsf_ienumtfpropertyvalue_skip_ref, msctf/IEnumTfPropertyValue::Skip, tsf.ienumtfpropertyvalue_skip
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - IEnumTfPropertyValue.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# IEnumTfPropertyValue::Skip


## -description




## -parameters




### -param ulCount [in]

Contains the number of elements to skip.


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
The method reached the end of the enumeration before the specified number of elements could be skipped.

</td>
</tr>
</table>
 



