---
UID: NF:msctf.ITfInputProcessorProfiles.EnumInputProcessorInfo
title: ITfInputProcessorProfiles::EnumInputProcessorInfo (msctf.h)
description: ITfInputProcessorProfiles::EnumInputProcessorInfo method
helpviewer_keywords: ["EnumInputProcessorInfo","EnumInputProcessorInfo method [Text Services Framework]","EnumInputProcessorInfo method [Text Services Framework]","ITfInputProcessorProfiles interface","ITfInputProcessorProfiles interface [Text Services Framework]","EnumInputProcessorInfo method","ITfInputProcessorProfiles.EnumInputProcessorInfo","ITfInputProcessorProfiles::EnumInputProcessorInfo","_tsf_itfinputprocessorprofiles_enuminputprocessorinfo_ref","msctf/ITfInputProcessorProfiles::EnumInputProcessorInfo","tsf.itfinputprocessorprofiles_enuminputprocessorinfo"]
old-location: tsf\itfinputprocessorprofiles_enuminputprocessorinfo.htm
tech.root: TSF
ms.assetid: 55b85ff3-35da-4126-861a-2aa4e2e8422f
ms.date: 12/05/2018
ms.keywords: EnumInputProcessorInfo, EnumInputProcessorInfo method [Text Services Framework], EnumInputProcessorInfo method [Text Services Framework],ITfInputProcessorProfiles interface, ITfInputProcessorProfiles interface [Text Services Framework],EnumInputProcessorInfo method, ITfInputProcessorProfiles.EnumInputProcessorInfo, ITfInputProcessorProfiles::EnumInputProcessorInfo, _tsf_itfinputprocessorprofiles_enuminputprocessorinfo_ref, msctf/ITfInputProcessorProfiles::EnumInputProcessorInfo, tsf.itfinputprocessorprofiles_enuminputprocessorinfo
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
 - ITfInputProcessorProfiles::EnumInputProcessorInfo
 - msctf/ITfInputProcessorProfiles::EnumInputProcessorInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfInputProcessorProfiles.EnumInputProcessorInfo
---

# ITfInputProcessorProfiles::EnumInputProcessorInfo


## -description

Obtains an enumerator that contains the class identifiers of all registered text services.

## -parameters

### -param ppEnum [out]

Pointer to an <b>IEnumGUID</b> interface pointer that receives the enumerator object. The enumerator contains the CLSID for each registered text service. The caller must release this object when it is no longer required.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppEnum</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation error occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register">ITfInputProcessorProfiles::Register
      </a>