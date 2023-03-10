---
UID: NF:msctf.IEnumTfInputProcessorProfiles.Clone
title: IEnumTfInputProcessorProfiles::Clone (msctf.h)
description: The IEnumTfInputProcessorProfiles::Clone method creates a copy of the enumerator object.
helpviewer_keywords: ["Clone","Clone method [Text Services Framework]","Clone method [Text Services Framework]","IEnumTfInputProcessorProfiles interface","IEnumTfInputProcessorProfiles interface [Text Services Framework]","Clone method","IEnumTfInputProcessorProfiles.Clone","IEnumTfInputProcessorProfiles::Clone","msctf/IEnumTfInputProcessorProfiles::Clone","tsf.ienumtfinputprocessorprofiles_clone"]
old-location: tsf\ienumtfinputprocessorprofiles_clone.htm
tech.root: TSF
ms.assetid: 485c27ac-20da-4974-832c-8305d18b2c4b
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],IEnumTfInputProcessorProfiles interface, IEnumTfInputProcessorProfiles interface [Text Services Framework],Clone method, IEnumTfInputProcessorProfiles.Clone, IEnumTfInputProcessorProfiles::Clone, msctf/IEnumTfInputProcessorProfiles::Clone, tsf.ienumtfinputprocessorprofiles_clone
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
 - IEnumTfInputProcessorProfiles::Clone
 - msctf/IEnumTfInputProcessorProfiles::Clone
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
 - IEnumTfInputProcessorProfiles.Clone
---

# IEnumTfInputProcessorProfiles::Clone


## -description

The <b>IEnumTfInputProcessorProfiles::Clone</b> method creates a copy of the enumerator object.

## -parameters

### -param ppEnum [out]

[out] A pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-ienumtfinputprocessorprofiles">IEnumTfInputProcessorProfiles</a> interface.

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