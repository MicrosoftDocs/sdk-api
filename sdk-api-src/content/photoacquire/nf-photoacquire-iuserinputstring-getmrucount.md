---
UID: NF:photoacquire.IUserInputString.GetMruCount
title: IUserInputString::GetMruCount (photoacquire.h)
description: The GetMruCount method retrieves the number of items in the list of most recently used items.
helpviewer_keywords: ["GetMruCount","GetMruCount method [Picture Acquisition]","GetMruCount method [Picture Acquisition]","IUserInputString interface","IUserInputString interface [Picture Acquisition]","GetMruCount method","IUserInputString.GetMruCount","IUserInputString::GetMruCount","IUserInputStringGetMruCount","photoacquire/IUserInputString::GetMruCount","picacq.iuserinputstring_getmrucount"]
old-location: picacq\iuserinputstring_getmrucount.htm
tech.root: picacq
ms.assetid: 47f1a916-2d1e-4fe8-837b-3e9bf4e51c0b
ms.date: 12/05/2018
ms.keywords: GetMruCount, GetMruCount method [Picture Acquisition], GetMruCount method [Picture Acquisition],IUserInputString interface, IUserInputString interface [Picture Acquisition],GetMruCount method, IUserInputString.GetMruCount, IUserInputString::GetMruCount, IUserInputStringGetMruCount, photoacquire/IUserInputString::GetMruCount, picacq.iuserinputstring_getmrucount
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
 - IUserInputString::GetMruCount
 - photoacquire/IUserInputString::GetMruCount
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
 - IUserInputString.GetMruCount
---

# IUserInputString::GetMruCount


## -description

The <code>GetMruCount</code> method retrieves the number of items in the list of most recently used items.

## -parameters

### -param pnMruCount [out]

Pointer to an integer value containing the number of items in the list of most recently used items.

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

## -remarks

If an error occurs, <i>pnMruCount</i> will be set to 0.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iuserinputstring">IUserInputString Interface</a>