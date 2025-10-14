---
UID: NF:vsprov.IVssSoftwareSnapshotProvider.QueryRevertStatus
title: IVssSoftwareSnapshotProvider::QueryRevertStatus (vsprov.h)
description: Returns an IVssAsync interface pointer that can be used to determine the status of the revert operation. (IVssSoftwareSnapshotProvider.QueryRevertStatus)
helpviewer_keywords: ["IVssSoftwareSnapshotProvider interface","QueryRevertStatus method","IVssSoftwareSnapshotProvider.QueryRevertStatus","IVssSoftwareSnapshotProvider::QueryRevertStatus","QueryRevertStatus","QueryRevertStatus method","QueryRevertStatus method","IVssSoftwareSnapshotProvider interface","base.ivsssoftwaresnapshotprovider_queryrevertstatus","vsprov/IVssSoftwareSnapshotProvider::QueryRevertStatus"]
old-location: base\ivsssoftwaresnapshotprovider_queryrevertstatus.htm
tech.root: base
ms.assetid: 05c70761-d839-4333-a5d6-6bd8b95851bb
ms.date: 12/05/2018
ms.keywords: IVssSoftwareSnapshotProvider interface,QueryRevertStatus method, IVssSoftwareSnapshotProvider.QueryRevertStatus, IVssSoftwareSnapshotProvider::QueryRevertStatus, QueryRevertStatus, QueryRevertStatus method, QueryRevertStatus method,IVssSoftwareSnapshotProvider interface, base.ivsssoftwaresnapshotprovider_queryrevertstatus, vsprov/IVssSoftwareSnapshotProvider::QueryRevertStatus
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssSoftwareSnapshotProvider::QueryRevertStatus
 - vsprov/IVssSoftwareSnapshotProvider::QueryRevertStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssSoftwareSnapshotProvider.QueryRevertStatus
---

# IVssSoftwareSnapshotProvider::QueryRevertStatus


## -description

Returns an <a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface pointer that can be used to determine the status of the revert operation.

## -parameters

### -param pwszVolume [in]

Null-terminated wide character string containing the volume name. The name must be in one of the following formats and must include a trailing backslash (\\): 




<ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example, D:\</li>
<li>A volume GUID path of the form \\?&#92;<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
</ul>

### -param ppAsync [out]

Pointer to a location that will receive an <a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface pointer that can be used to retrieve the status of the revert operation. When the operation is complete, the caller must release the interface pointer by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

## -returns

The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The status of the revert operation was successfully queried.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient backup privileges or is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszVolume</i> parameter does not specify a valid volume.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_VOLUME_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The revert operation is not supported on this volume.

</td>
</tr>
</table>

## -remarks

The revert operation will continue even if the computer is rebooted, and cannot be canceled or undone, except by restoring a backup that was created using another method. The <a href="/windows/desktop/api/vss/nf-vss-ivssasync-querystatus">IVssAsync::QueryStatus</a> method cannot return VSS_S_ASYNC_CANCELLED, because the revert operation cannot be canceled after it has started.

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivsssoftwaresnapshotprovider">IVssSoftwareSnapshotProvider</a>
