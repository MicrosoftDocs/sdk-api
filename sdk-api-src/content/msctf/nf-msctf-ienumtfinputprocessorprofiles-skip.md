---
UID: NF:msctf.IEnumTfInputProcessorProfiles.Skip
title: IEnumTfInputProcessorProfiles::Skip (msctf.h)
description: The IEnumTfInputProcessorProfiles::Skip method moves the current position forward in the enumeration sequence by the specified number of elements.
helpviewer_keywords: ["IEnumTfInputProcessorProfiles interface [Text Services Framework]","Skip method","IEnumTfInputProcessorProfiles.Skip","IEnumTfInputProcessorProfiles::Skip","Skip","Skip method [Text Services Framework]","Skip method [Text Services Framework]","IEnumTfInputProcessorProfiles interface","msctf/IEnumTfInputProcessorProfiles::Skip","tsf.ienumtfinputprocessorprofiles_skip"]
old-location: tsf\ienumtfinputprocessorprofiles_skip.htm
tech.root: TSF
ms.assetid: 7b0bf0be-1f0d-4da9-a8d2-c8a29ae3dcac
ms.date: 12/05/2018
ms.keywords: IEnumTfInputProcessorProfiles interface [Text Services Framework],Skip method, IEnumTfInputProcessorProfiles.Skip, IEnumTfInputProcessorProfiles::Skip, Skip, Skip method [Text Services Framework], Skip method [Text Services Framework],IEnumTfInputProcessorProfiles interface, msctf/IEnumTfInputProcessorProfiles::Skip, tsf.ienumtfinputprocessorprofiles_skip
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
 - IEnumTfInputProcessorProfiles::Skip
 - msctf/IEnumTfInputProcessorProfiles::Skip
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
 - IEnumTfInputProcessorProfiles.Skip
---

# IEnumTfInputProcessorProfiles::Skip


## -description

The <a href="/windows/desktop/api/msctf/nf-msctf-ienumtfinputprocessorprofiles-next">IEnumTfInputProcessorProfiles::Skip</a> method moves the current position forward in the enumeration sequence by the specified number of elements.

## -parameters

### -param ulCount [in]

[in] Contains the number of elements to skip.

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
<dt><b>E_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method reached the end of the enumeration before the specified number of elements could be skipped.

</td>
</tr>
</table>