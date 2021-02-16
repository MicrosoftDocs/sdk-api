---
UID: NF:winsync.ISingleItemException.GetItemId
title: ISingleItemException::GetItemId (winsync.h)
description: Gets the ID of the item that is specified in the exception.
helpviewer_keywords: ["GetItemId","GetItemId method [Windows Sync]","GetItemId method [Windows Sync]","ISingleItemException interface","ISingleItemException interface [Windows Sync]","GetItemId method","ISingleItemException.GetItemId","ISingleItemException::GetItemId","winsync.isingleitemexception_getitemid","winsync/ISingleItemException::GetItemId"]
old-location: winsync\isingleitemexception_getitemid.htm
tech.root: winsync
ms.assetid: 1bcea395-d383-434f-b3a6-cffd4419fce3
ms.date: 12/05/2018
ms.keywords: GetItemId, GetItemId method [Windows Sync], GetItemId method [Windows Sync],ISingleItemException interface, ISingleItemException interface [Windows Sync],GetItemId method, ISingleItemException.GetItemId, ISingleItemException::GetItemId, winsync.isingleitemexception_getitemid, winsync/ISingleItemException::GetItemId
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISingleItemException::GetItemId
 - winsync/ISingleItemException::GetItemId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISingleItemException.GetItemId
---

# ISingleItemException::GetItemId


## -description

Gets the ID of the item that is specified in the exception.

## -parameters

### -param pbItemId [in, out]

Returns the ID of the item that is specified in the exception.

### -param pcbIdSize [in, out]

Specifies the number of bytes in <i>pbItemId</i>. Returns the number of bytes required to retrieve the ID when <i>pbItemId</i> is too small, or returns the number of bytes written.

## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

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
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pbItemId</i> is too small. In this case, the required number of bytes is returned in <i>pcbIdSize</i>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isingleitemexception">ISingleItemException Interface</a>