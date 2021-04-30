---
UID: NF:winsync.IChangeUnitException.GetItemId
title: IChangeUnitException::GetItemId (winsync.h)
description: Gets the item ID for the item that contains the change unit that is associated with the exception.
helpviewer_keywords: ["GetItemId","GetItemId method [Windows Sync]","GetItemId method [Windows Sync]","IChangeUnitException interface","IChangeUnitException interface [Windows Sync]","GetItemId method","IChangeUnitException.GetItemId","IChangeUnitException::GetItemId","winsync.ichangeunitexception_getitemid","winsync/IChangeUnitException::GetItemId"]
old-location: winsync\ichangeunitexception_getitemid.htm
tech.root: winsync
ms.assetid: d5c76ecf-bd3f-4a0a-9fba-4fd51591d39f
ms.date: 12/05/2018
ms.keywords: GetItemId, GetItemId method [Windows Sync], GetItemId method [Windows Sync],IChangeUnitException interface, IChangeUnitException interface [Windows Sync],GetItemId method, IChangeUnitException.GetItemId, IChangeUnitException::GetItemId, winsync.ichangeunitexception_getitemid, winsync/IChangeUnitException::GetItemId
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
 - IChangeUnitException::GetItemId
 - winsync/IChangeUnitException::GetItemId
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
 - IChangeUnitException.GetItemId
---

# IChangeUnitException::GetItemId


## -description

Gets the item ID for the item that contains the change unit that is associated with the exception.

## -parameters

### -param pbItemId [in, out]

Returns the item ID that contains the change unit that is associated with the exception.

### -param pcbIdSize [in, out]

Specifies the number of bytes in <i>pbItemId</i>. Returns the number of bytes required to retrieve the ID when <i>pbItemId</i> is too small, or the number of bytes written.

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
<dt><b>E_INVALIDARG</b></dt>
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

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeunitexception">IChangeUnitException Interface</a>