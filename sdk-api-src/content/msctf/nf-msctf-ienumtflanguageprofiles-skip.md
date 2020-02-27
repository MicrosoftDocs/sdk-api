---
UID: NF:msctf.IEnumTfLanguageProfiles.Skip
title: IEnumTfLanguageProfiles::Skip (msctf.h)
description: IEnumTfLanguageProfiles::Skip method
old-location: tsf\ienumtflanguageprofiles_skip.htm
tech.root: TSF
ms.assetid: 67e6d841-a3e9-4e55-ac35-9197f256d9bf
ms.date: 12/05/2018
ms.keywords: IEnumTfLanguageProfiles interface [Text Services Framework],Skip method, IEnumTfLanguageProfiles.Skip, IEnumTfLanguageProfiles::Skip, Skip, Skip method [Text Services Framework], Skip method [Text Services Framework],IEnumTfLanguageProfiles interface, _tsf_ienumtflanguageprofiles_skip_ref, msctf/IEnumTfLanguageProfiles::Skip, tsf.ienumtflanguageprofiles_skip
f1_keywords:
- msctf/IEnumTfLanguageProfiles.Skip
dev_langs:
- c++
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
- IEnumTfLanguageProfiles.Skip
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# IEnumTfLanguageProfiles::Skip


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
 



