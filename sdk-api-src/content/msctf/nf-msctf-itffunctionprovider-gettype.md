---
UID: NF:msctf.ITfFunctionProvider.GetType
title: ITfFunctionProvider::GetType
author: windows-driver-content
description: ITfFunctionProvider::GetType method
old-location: tsf\itffunctionprovider_gettype.htm
old-project: TSF
ms.assetid: fff9ad62-f777-423c-a59d-ebd7d99da6a9
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: GetType, GetType method [Text Services Framework], GetType method [Text Services Framework],ITfFunctionProvider interface, ITfFunctionProvider interface [Text Services Framework],GetType method, ITfFunctionProvider.GetType, ITfFunctionProvider::GetType, _tsf_itffunctionprovider_gettype_ref, msctf/ITfFunctionProvider::GetType, tsf.itffunctionprovider_gettype
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
-	ITfFunctionProvider.GetType
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfFunctionProvider::GetType


## -description




## -parameters




### -param pguid [out]

Pointer to a GUID value that receives the type identifier of the function provider.


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
The method was successful

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pguid</i> is invalid.

</td>
</tr>
</table>
 



