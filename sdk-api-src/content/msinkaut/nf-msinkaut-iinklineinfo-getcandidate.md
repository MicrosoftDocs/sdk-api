---
UID: NF:msinkaut.IInkLineInfo.GetCandidate
title: IInkLineInfo::GetCandidate (msinkaut.h)
description: Returns one recognition alternate from the recognition result list.
helpviewer_keywords: ["59005f51-7052-4aef-915d-4c939eecec99","GetCandidate","GetCandidate method [Tablet PC]","GetCandidate method [Tablet PC]","IInkLineInfo interface","IInkLineInfo interface [Tablet PC]","GetCandidate method","IInkLineInfo.GetCandidate","IInkLineInfo::GetCandidate","msinkaut/IInkLineInfo::GetCandidate","tablet.iinklineinfo_getcandidate"]
old-location: tablet\iinklineinfo_getcandidate.htm
tech.root: tablet
ms.assetid: 59005f51-7052-4aef-915d-4c939eecec99
ms.date: 12/05/2018
ms.keywords: 59005f51-7052-4aef-915d-4c939eecec99, GetCandidate, GetCandidate method [Tablet PC], GetCandidate method [Tablet PC],IInkLineInfo interface, IInkLineInfo interface [Tablet PC],GetCandidate method, IInkLineInfo.GetCandidate, IInkLineInfo::GetCandidate, msinkaut/IInkLineInfo::GetCandidate, tablet.iinklineinfo_getcandidate
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkLineInfo::GetCandidate
 - msinkaut/IInkLineInfo::GetCandidate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkLineInfo.GetCandidate
---

# IInkLineInfo::GetCandidate


## -description

Returns one recognition alternate from the recognition result list.

## -parameters

### -param nCandidateNum [in]

Zero-based index of the alternate list entry to retrieve.

### -param pwcRecogWord [out]

Buffer in which to store the selected recognition alternate. If <i>pwcRecogWord</i> is <b>NULL</b>, the method does not attempt to retrieve the recognition alternate word.

### -param pcwcRecogWord [out]

Passes the length of the <i>pwcRecogWord</i> buffer in Unicode characters, and returns the number of Unicode characters that were copied into the buffer.

### -param dwFlags [in]

Not used.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The <i>nCandidateNum</i> index is greater that the number of recognition alternates.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwcRecogWord</i> buffer is not large enough to accept the recognition alternate.

</td>
</tr>
</table>

## -remarks

If the <i>pwcRecogWord</i> parameter is null, the method does not attempt to retrieve the recognition alternate word, but only sets <i>pwcRecogWord</i> to the number of characters in the recognition alternate.

If the <i>pwcRecogWord</i> buffer is not large enough to contain the recognition alternate, then the <i>pwcRecogWord</i> buffer is filled with the first <i>pwcRecogWord</i> number of characters from the recognition alternate.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinklineinfo">IInkLineInfo</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-setcandidate">SetCandidate Method</a>