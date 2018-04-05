---
UID: NF:msctf.ITfDisplayAttributeInfo.GetAttributeInfo
title: ITfDisplayAttributeInfo::GetAttributeInfo method
author: windows-driver-content
description: ITfDisplayAttributeInfo::GetAttributeInfo method
old-location: tsf\itfdisplayattributeinfo_getattributeinfo.htm
old-project: TSF
ms.assetid: 32e28feb-1186-4848-a9d4-70b27f865d3c
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetAttributeInfo method [Text Services Framework], GetAttributeInfo method [Text Services Framework], ITfDisplayAttributeInfo interface, GetAttributeInfo,ITfDisplayAttributeInfo.GetAttributeInfo, ITfDisplayAttributeInfo, ITfDisplayAttributeInfo interface [Text Services Framework], GetAttributeInfo method, ITfDisplayAttributeInfo::GetAttributeInfo, _tsf_itfdisplayattributeinfo_getattributeinfo_ref, msctf/ITfDisplayAttributeInfo::GetAttributeInfo, tsf.itfdisplayattributeinfo_getattributeinfo
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
-	ITfDisplayAttributeInfo.GetAttributeInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfDisplayAttributeInfo::GetAttributeInfo method


## -description




## -parameters




### -param pda [out]

Pointer to a <a href="https://msdn.microsoft.com/29faaa22-ea03-4a2e-a035-7979e2a89fc9">TF_DISPLAYATTRIBUTE</a> structure that receives display attribute data.


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
<i>pda</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7f590ecf-06e9-42da-ba40-4364296ae594">ITfDisplayAttributeInfo</a>



<a href="https://msdn.microsoft.com/29faaa22-ea03-4a2e-a035-7979e2a89fc9">TF_DISPLAYATTRIBUTE
      </a>
 

 

