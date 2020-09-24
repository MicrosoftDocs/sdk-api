---
UID: NF:photoacquire.IUserInputString.GetMruEntryAt
title: IUserInputString::GetMruEntryAt (photoacquire.h)
description: The GetMruEntryAt method retrieves the entry at the given index in the most recently used list.
helpviewer_keywords: ["GetMruEntryAt","GetMruEntryAt method [Picture Acquisition]","GetMruEntryAt method [Picture Acquisition]","IUserInputString interface","IUserInputString interface [Picture Acquisition]","GetMruEntryAt method","IUserInputString.GetMruEntryAt","IUserInputString::GetMruEntryAt","IUserInputStringGetMruEntryAt","photoacquire/IUserInputString::GetMruEntryAt","picacq.iuserinputstring_getmruentryat"]
old-location: picacq\iuserinputstring_getmruentryat.htm
tech.root: picacq
ms.assetid: d03c3eba-e55c-421d-acfa-fea6aa645cc5
ms.date: 12/05/2018
ms.keywords: GetMruEntryAt, GetMruEntryAt method [Picture Acquisition], GetMruEntryAt method [Picture Acquisition],IUserInputString interface, IUserInputString interface [Picture Acquisition],GetMruEntryAt method, IUserInputString.GetMruEntryAt, IUserInputString::GetMruEntryAt, IUserInputStringGetMruEntryAt, photoacquire/IUserInputString::GetMruEntryAt, picacq.iuserinputstring_getmruentryat
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
 - IUserInputString::GetMruEntryAt
 - photoacquire/IUserInputString::GetMruEntryAt
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
 - IUserInputString.GetMruEntryAt
---

# IUserInputString::GetMruEntryAt


## -description

The <code>GetMruEntryAt</code> method retrieves the entry at the given index in the most recently used list.

## -parameters

### -param nIndex [in]

Integer containing the index at which to retrieve the entry.

### -param pbstrMruEntry [out]

Pointer to a string containing the most recently used entry.

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