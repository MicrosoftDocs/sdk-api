---
UID: NF:photoacquire.IUserInputString.GetMaxLength
title: IUserInputString::GetMaxLength (photoacquire.h)
description: The GetMaxLength method retrieves the maximum string length the user interface (UI) should allow.
helpviewer_keywords: ["GetMaxLength","GetMaxLength method [Picture Acquisition]","GetMaxLength method [Picture Acquisition]","IUserInputString interface","IUserInputString interface [Picture Acquisition]","GetMaxLength method","IUserInputString.GetMaxLength","IUserInputString::GetMaxLength","IUserInputStringGetMaxLength","photoacquire/IUserInputString::GetMaxLength","picacq.iuserinputstring_getmaxlength"]
old-location: picacq\iuserinputstring_getmaxlength.htm
tech.root: picacq
ms.assetid: 474b32f5-e8b3-49d2-a2de-a78244b9066e
ms.date: 12/05/2018
ms.keywords: GetMaxLength, GetMaxLength method [Picture Acquisition], GetMaxLength method [Picture Acquisition],IUserInputString interface, IUserInputString interface [Picture Acquisition],GetMaxLength method, IUserInputString.GetMaxLength, IUserInputString::GetMaxLength, IUserInputStringGetMaxLength, photoacquire/IUserInputString::GetMaxLength, picacq.iuserinputstring_getmaxlength
req.header: photoacquire.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUserInputString::GetMaxLength
 - photoacquire/IUserInputString::GetMaxLength
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IUserInputString.GetMaxLength
---

# IUserInputString::GetMaxLength


## -description

The <code>GetMaxLength</code> method retrieves the maximum string length the user interface (UI) should allow.

## -parameters

### -param pcchMaxLength [out]

Pointer to the size of the maximum string length in characters.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was passed where a non-<b>NULL</b> pointer is expected.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iuserinputstring">IUserInputString Interface</a>