---
UID: NF:msctf.IEnumTfDocumentMgrs.Skip
title: IEnumTfDocumentMgrs::Skip (msctf.h)
description: IEnumTfDocumentMgrs::Skip method
helpviewer_keywords: ["IEnumTfDocumentMgrs interface [Text Services Framework]","Skip method","IEnumTfDocumentMgrs.Skip","IEnumTfDocumentMgrs::Skip","Skip","Skip method [Text Services Framework]","Skip method [Text Services Framework]","IEnumTfDocumentMgrs interface","_tsf_ienumtfdocumentmgrs_skip_ref","msctf/IEnumTfDocumentMgrs::Skip","tsf.ienumtfdocumentmgrs_skip"]
old-location: tsf\ienumtfdocumentmgrs_skip.htm
tech.root: TSF
ms.assetid: 04464160-d171-4c83-91f0-068a1c13544a
ms.date: 12/05/2018
ms.keywords: IEnumTfDocumentMgrs interface [Text Services Framework],Skip method, IEnumTfDocumentMgrs.Skip, IEnumTfDocumentMgrs::Skip, Skip, Skip method [Text Services Framework], Skip method [Text Services Framework],IEnumTfDocumentMgrs interface, _tsf_ienumtfdocumentmgrs_skip_ref, msctf/IEnumTfDocumentMgrs::Skip, tsf.ienumtfdocumentmgrs_skip
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
 - IEnumTfDocumentMgrs::Skip
 - msctf/IEnumTfDocumentMgrs::Skip
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
 - IEnumTfDocumentMgrs.Skip
---

# IEnumTfDocumentMgrs::Skip


## -description

Moves the current position forward in the enumeration sequence by the specified number of elements.

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

## -see-also

[IEnumTfDocumentMgrs interface](nn-msctf-ienumtfdocumentmgrs.md), [ITfDocumentMgr interface](nn-msctf-itfdocumentmgr.md)

