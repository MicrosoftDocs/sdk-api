---
UID: NF:msctf.IEnumTfLanguageProfiles.Next
title: IEnumTfLanguageProfiles::Next (msctf.h)
author: windows-sdk-content
description: IEnumTfLanguageProfiles::Next method
old-location: tsf\ienumtflanguageprofiles_next.htm
tech.root: TSF
ms.assetid: 790fb0f4-4abd-4947-8e9a-68739657a8f8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumTfLanguageProfiles interface [Text Services Framework],Next method, IEnumTfLanguageProfiles.Next, IEnumTfLanguageProfiles::Next, Next, Next method [Text Services Framework], Next method [Text Services Framework],IEnumTfLanguageProfiles interface, _tsf_ienumtflanguageprofiles_next_ref, msctf/IEnumTfLanguageProfiles::Next, tsf.ienumtflanguageprofiles_next
ms.topic: method
f1_keywords: 
 - "msctf/IEnumTfLanguageProfiles.Next"
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IEnumTfLanguageProfiles.Next
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# IEnumTfLanguageProfiles::Next


## -description




## -parameters




### -param ulCount [in]

Specifies the number of elements to obtain.


### -param pProfile [out]

Pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/msctf/ns-msctf-tf_languageprofile">TF_LANGUAGEPROFILE</a> structures that receives the requested data. This array must be at least <i>ulCount</i> elements in size.


### -param pcFetch [out]

Pointer to a ULONG value that receives the number of elements obtained. This value can be less than the number of items requested. This parameter can be <b>NULL</b>.


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
<i>pProfile</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-ienumtflanguageprofiles">IEnumTfLanguageProfiles</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/ns-msctf-tf_languageprofile">TF_LANGUAGEPROFILE
      </a>
 

 

