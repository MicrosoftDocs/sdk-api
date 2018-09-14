---
UID: NF:msctf.ITextStoreACPServices.CreateRange
title: ITextStoreACPServices::CreateRange
author: windows-sdk-content
description: ITextStoreACPServices::CreateRange method
old-location: tsf\itextstoreacpservices_createrange.htm
tech.root: TSF
ms.assetid: 727945e7-b876-460e-9b06-8d03734f53b2
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CreateRange, CreateRange method [Text Services Framework], CreateRange method [Text Services Framework],ITextStoreACPServices interface, ITextStoreACPServices interface [Text Services Framework],CreateRange method, ITextStoreACPServices.CreateRange, ITextStoreACPServices::CreateRange, _tsf_itextstoreacpservices_createrange_ref, msctf/ITextStoreACPServices::CreateRange, tsf.itextstoreacpservices_createrange
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
 - ITextStoreACPServices.CreateRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreACPServices::CreateRange


## -description




## -parameters




### -param acpStart [in]

Contains the starting position of the range.


### -param acpEnd [in]

Contains the ending position of the range.


### -param ppRange [out]

Pointer to an <a href="https://msdn.microsoft.com/aaa497ca-4cf2-401a-a6d8-cc8a75479cc4">ITfRangeACP</a> interface pointer that receives the range object.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppRange</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8c84429c-3f99-4ab1-b994-e4e93cd9c86d">ITextStoreACPServices</a>



<a href="https://msdn.microsoft.com/aaa497ca-4cf2-401a-a6d8-cc8a75479cc4">ITfRangeACP
      </a>
 

 

