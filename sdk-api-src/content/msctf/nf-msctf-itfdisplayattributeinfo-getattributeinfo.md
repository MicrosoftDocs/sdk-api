---
UID: NF:msctf.ITfDisplayAttributeInfo.GetAttributeInfo
title: ITfDisplayAttributeInfo::GetAttributeInfo (msctf.h)
author: windows-sdk-content
description: ITfDisplayAttributeInfo::GetAttributeInfo method
old-location: tsf\itfdisplayattributeinfo_getattributeinfo.htm
tech.root: TSF
ms.assetid: 32e28feb-1186-4848-a9d4-70b27f865d3c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAttributeInfo, GetAttributeInfo method [Text Services Framework], GetAttributeInfo method [Text Services Framework],ITfDisplayAttributeInfo interface, ITfDisplayAttributeInfo interface [Text Services Framework],GetAttributeInfo method, ITfDisplayAttributeInfo.GetAttributeInfo, ITfDisplayAttributeInfo::GetAttributeInfo, _tsf_itfdisplayattributeinfo_getattributeinfo_ref, msctf/ITfDisplayAttributeInfo::GetAttributeInfo, tsf.itfdisplayattributeinfo_getattributeinfo
ms.topic: method
f1_keywords: ["msctf/ITfDisplayAttributeInfo.GetAttributeInfo"]
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
 - Msctf.dll
api_name:
 - ITfDisplayAttributeInfo.GetAttributeInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfDisplayAttributeInfo::GetAttributeInfo


## -description




## -parameters




### -param pda [out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/msctf/ns-msctf-tf_displayattribute">TF_DISPLAYATTRIBUTE</a> structure that receives display attribute data.


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




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfdisplayattributeinfo">ITfDisplayAttributeInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/ns-msctf-tf_displayattribute">TF_DISPLAYATTRIBUTE
      </a>
 

 

