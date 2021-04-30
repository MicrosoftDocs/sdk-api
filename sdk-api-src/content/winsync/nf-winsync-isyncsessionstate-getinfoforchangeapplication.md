---
UID: NF:winsync.ISyncSessionState.GetInfoForChangeApplication
title: ISyncSessionState::GetInfoForChangeApplication (winsync.h)
description: Retrieves stored data for a serialized change applier.
helpviewer_keywords: ["GetInfoForChangeApplication","GetInfoForChangeApplication method [Windows Sync]","GetInfoForChangeApplication method [Windows Sync]","ISyncSessionState interface","ISyncSessionState interface [Windows Sync]","GetInfoForChangeApplication method","ISyncSessionState.GetInfoForChangeApplication","ISyncSessionState::GetInfoForChangeApplication","winsync.isyncsessionstate_getinfoforchangeapplication","winsync/ISyncSessionState::GetInfoForChangeApplication"]
old-location: winsync\isyncsessionstate_getinfoforchangeapplication.htm
tech.root: winsync
ms.assetid: 88f7f8f7-468f-4d9d-9593-0d3f92cb458f
ms.date: 12/05/2018
ms.keywords: GetInfoForChangeApplication, GetInfoForChangeApplication method [Windows Sync], GetInfoForChangeApplication method [Windows Sync],ISyncSessionState interface, ISyncSessionState interface [Windows Sync],GetInfoForChangeApplication method, ISyncSessionState.GetInfoForChangeApplication, ISyncSessionState::GetInfoForChangeApplication, winsync.isyncsessionstate_getinfoforchangeapplication, winsync/ISyncSessionState::GetInfoForChangeApplication
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
 - ISyncSessionState::GetInfoForChangeApplication
 - winsync/ISyncSessionState::GetInfoForChangeApplication
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
 - ISyncSessionState.GetInfoForChangeApplication
---

# ISyncSessionState::GetInfoForChangeApplication


## -description

Retrieves stored data for a serialized change applier.

## -parameters

### -param pbChangeApplierInfo [in, out]

Returns the serialized change applier data.

### -param pcbChangeApplierInfo [in, out]

Specifies the number of bytes in <i>pbChangeApplierInfo</i>. Returns the number of bytes required to retrieve the change applier data when <i>pcbChangeApplierInfo</i> is too small, or returns the number of bytes written.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

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
<i>pbChangeApplierInfo</i> is too small. In this case, the required number of bytes is returned in <i>pcbChangeApplierInfo</i>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncsessionstate">ISyncSessionState Interface</a>