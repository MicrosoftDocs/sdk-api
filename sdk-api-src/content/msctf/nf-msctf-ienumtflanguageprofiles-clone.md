---
UID: NF:msctf.IEnumTfLanguageProfiles.Clone
title: IEnumTfLanguageProfiles::Clone (msctf.h)
description: IEnumTfLanguageProfiles::Clone method
helpviewer_keywords: ["Clone","Clone method [Text Services Framework]","Clone method [Text Services Framework]","IEnumTfLanguageProfiles interface","IEnumTfLanguageProfiles interface [Text Services Framework]","Clone method","IEnumTfLanguageProfiles.Clone","IEnumTfLanguageProfiles::Clone","_tsf_ienumtflanguageprofiles_clone_ref","msctf/IEnumTfLanguageProfiles::Clone","tsf.ienumtflanguageprofiles_clone"]
old-location: tsf\ienumtflanguageprofiles_clone.htm
tech.root: TSF
ms.assetid: 77fbb195-b3c8-4254-a4d9-117ea8052951
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],IEnumTfLanguageProfiles interface, IEnumTfLanguageProfiles interface [Text Services Framework],Clone method, IEnumTfLanguageProfiles.Clone, IEnumTfLanguageProfiles::Clone, _tsf_ienumtflanguageprofiles_clone_ref, msctf/IEnumTfLanguageProfiles::Clone, tsf.ienumtflanguageprofiles_clone
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - IEnumTfLanguageProfiles::Clone
 - msctf/IEnumTfLanguageProfiles::Clone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - IEnumTfLanguageProfiles.Clone
---

# IEnumTfLanguageProfiles::Clone


## -description

Creates a copy of the enumerator object.

## -parameters

### -param ppEnum [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-ienumtflanguageprofiles">IEnumTfLanguageProfiles</a> interface pointer that receives the new enumerator.

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

[IEnumTfLanguageProfiles interface](nn-msctf-ienumtflanguageprofiles.md), [TF_LANGUAGEPROFILE](ns-msctf-tf_languageprofile.md)