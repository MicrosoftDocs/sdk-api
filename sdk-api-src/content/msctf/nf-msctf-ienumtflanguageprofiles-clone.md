---
UID: NF:msctf.IEnumTfLanguageProfiles.Clone
title: IEnumTfLanguageProfiles::Clone (msctf.h)
author: windows-sdk-content
description: IEnumTfLanguageProfiles::Clone method
old-location: tsf\ienumtflanguageprofiles_clone.htm
tech.root: TSF
ms.assetid: 77fbb195-b3c8-4254-a4d9-117ea8052951
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],IEnumTfLanguageProfiles interface, IEnumTfLanguageProfiles interface [Text Services Framework],Clone method, IEnumTfLanguageProfiles.Clone, IEnumTfLanguageProfiles::Clone, _tsf_ienumtflanguageprofiles_clone_ref, msctf/IEnumTfLanguageProfiles::Clone, tsf.ienumtflanguageprofiles_clone
ms.topic: method
f1_keywords: 
 - "msctf/IEnumTfLanguageProfiles.Clone"
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
 - IEnumTfLanguageProfiles.Clone
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# IEnumTfLanguageProfiles::Clone


## -description




## -parameters




### -param ppEnum [out]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-ienumtflanguageprofiles">IEnumTfLanguageProfiles</a> interface pointer that receives the new enumerator.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-ienumtflanguageprofiles">IEnumTfLanguageProfiles
      </a>
 

 

