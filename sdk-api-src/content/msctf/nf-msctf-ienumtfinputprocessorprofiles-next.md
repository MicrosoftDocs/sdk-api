---
UID: NF:msctf.IEnumTfInputProcessorProfiles.Next
title: IEnumTfInputProcessorProfiles::Next (msctf.h)
description: The IEnumTfInputProcessorProfiles::Next method obtains, from the current position, the specified number of elements in the enumeration sequence.
helpviewer_keywords: ["IEnumTfInputProcessorProfiles interface [Text Services Framework]","Next method","IEnumTfInputProcessorProfiles.Next","IEnumTfInputProcessorProfiles::Next","Next","Next method [Text Services Framework]","Next method [Text Services Framework]","IEnumTfInputProcessorProfiles interface","msctf/IEnumTfInputProcessorProfiles::Next","tsf.ienumtfinputprocessorprofiles_next"]
old-location: tsf\ienumtfinputprocessorprofiles_next.htm
tech.root: TSF
ms.assetid: b936c479-a5f1-47a3-bd5a-f1b83cd84dc0
ms.date: 12/05/2018
ms.keywords: IEnumTfInputProcessorProfiles interface [Text Services Framework],Next method, IEnumTfInputProcessorProfiles.Next, IEnumTfInputProcessorProfiles::Next, Next, Next method [Text Services Framework], Next method [Text Services Framework],IEnumTfInputProcessorProfiles interface, msctf/IEnumTfInputProcessorProfiles::Next, tsf.ienumtfinputprocessorprofiles_next
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - IEnumTfInputProcessorProfiles::Next
 - msctf/IEnumTfInputProcessorProfiles::Next
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
 - IEnumTfInputProcessorProfiles.Next
---

# IEnumTfInputProcessorProfiles::Next


## -description

The <b>IEnumTfInputProcessorProfiles::Next</b> method obtains, from the current position, the specified number of elements in the enumeration sequence.

## -parameters

### -param ulCount [in]

[in] Specifies the number of elements to obtain.

### -param pProfile [out]

[out] Pointer to an array of <a href="/windows/desktop/api/msctf/ns-msctf-tf_inputprocessorprofile">TF_INPUTPROCESSORPROFILE</a> structures. This array must be at least <i>ulCount</i> elements in size.

### -param pcFetch [out]

[out] Pointer to a ULONG value that receives the number of elements actually obtained. This value can be less than the number of items requested. This parameter can be <b>NULL</b>.

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
One or more parameters are invalid.

</td>
</tr>
</table>