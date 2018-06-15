---
UID: NF:vsprov.IVssSoftwareSnapshotProvider.QueryRevertStatus
title: IVssSoftwareSnapshotProvider::QueryRevertStatus
author: windows-sdk-content
description: Returns an IVssAsync interface pointer that can be used to determine the status of the revert operation.
old-location: base\ivsssoftwaresnapshotprovider_queryrevertstatus.htm
old-project: VSS
ms.assetid: 05c70761-d839-4333-a5d6-6bd8b95851bb
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IVssSoftwareSnapshotProvider interface,QueryRevertStatus method, IVssSoftwareSnapshotProvider.QueryRevertStatus, IVssSoftwareSnapshotProvider::QueryRevertStatus, QueryRevertStatus, QueryRevertStatus method, QueryRevertStatus method,IVssSoftwareSnapshotProvider interface, base.ivsssoftwaresnapshotprovider_queryrevertstatus, vsprov/IVssSoftwareSnapshotProvider::QueryRevertStatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VSS_MGMT_OBJECT_UNION, *PVSS_MGMT_OBJECT_UNION
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
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssSoftwareSnapshotProvider::QueryRevertStatus


## -description


Returns an <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> interface pointer that can be used to determine the status of the revert operation.


## -parameters




### -param pwszVolume [in]

Null-terminated wide character string containing the volume name. The name must be in one of the following formats and must include a trailing backslash (\): 




<ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example, D:\</li>
<li>A volume GUID path of the form \\?\<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
</ul>

### -param ppAsync [out]

Pointer to a location that will receive an <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> interface pointer that can be used to retrieve the status of the revert operation. When the operation is complete, the caller must release the interface pointer by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.


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
<dt><b><b>VSS_E_OBJECT_NOT_FOUND</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszVolume</i> parameter does not specify a valid volume.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VSS_E_VOLUME_NOT_SUPPORTED</b></b></dt>
</dl>
</td>
<td width="60%">
The revert operation is not supported on this volume.

</td>
</tr>
</table>
 




## -remarks



The revert operation will continue even if the computer is rebooted, and cannot be canceled or undone, except by restoring a backup that was created using another method. The <a href="https://msdn.microsoft.com/85fb3ae8-dc09-4f6f-a96b-e4dc046ff48a">IVssAsync::QueryStatus</a> method cannot return VSS_S_ASYNC_CANCELLED, because the revert operation cannot be canceled after it has started.




## -see-also




<a href="https://msdn.microsoft.com/5c95f2fb-c132-489c-af48-2ffafad0b41f">IVssSoftwareSnapshotProvider</a>
 

 

