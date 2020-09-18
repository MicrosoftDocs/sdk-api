---
UID: NF:vsprov.IVssSoftwareSnapshotProvider.GetSnapshotProperties
title: IVssSoftwareSnapshotProvider::GetSnapshotProperties (vsprov.h)
description: Gets the properties of the specified shadow copy.
helpviewer_keywords: ["GetSnapshotProperties","GetSnapshotProperties method","GetSnapshotProperties method","IVssSoftwareSnapshotProvider interface","IVssSoftwareSnapshotProvider interface","GetSnapshotProperties method","IVssSoftwareSnapshotProvider.GetSnapshotProperties","IVssSoftwareSnapshotProvider::GetSnapshotProperties","base.ivsssoftwaresnapshotprovider_getsnapshotproperties","vsprov/IVssSoftwareSnapshotProvider::GetSnapshotProperties"]
old-location: base\ivsssoftwaresnapshotprovider_getsnapshotproperties.htm
tech.root: base
ms.assetid: 59886344-d594-4eb8-9718-ab11a6627e8e
ms.date: 12/05/2018
ms.keywords: GetSnapshotProperties, GetSnapshotProperties method, GetSnapshotProperties method,IVssSoftwareSnapshotProvider interface, IVssSoftwareSnapshotProvider interface,GetSnapshotProperties method, IVssSoftwareSnapshotProvider.GetSnapshotProperties, IVssSoftwareSnapshotProvider::GetSnapshotProperties, base.ivsssoftwaresnapshotprovider_getsnapshotproperties, vsprov/IVssSoftwareSnapshotProvider::GetSnapshotProperties
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
 - IVssSoftwareSnapshotProvider::GetSnapshotProperties
 - vsprov/IVssSoftwareSnapshotProvider::GetSnapshotProperties
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
 - IVssSoftwareSnapshotProvider.GetSnapshotProperties
---

# IVssSoftwareSnapshotProvider::GetSnapshotProperties


## -description

Gets the properties of the specified shadow copy.

## -parameters

### -param SnapshotId [in]

Shadow copy identifier.

### -param pProp [out]

The address of a caller-allocated <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure that receives the shadow copy properties. The provider is responsible for setting the members of this structure. All members are required except  <b>m_pwszExposedName</b> and <b>m_pwszExposedPath</b>, which the provider can set to <b>NULL</b>. The provider allocates memory for all string members  that it sets in the structure. When the structure is no longer needed, the caller is responsible for freeing these strings by calling the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-vssfreesnapshotproperties">VssFreeSnapshotProperties</a> function.

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
The requested information was successfully returned.

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
The specified volume was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">
Provider error. The provider logged the error in the event log. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>

## -remarks

The caller should set the contents of the <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure to zero before calling the <b>GetSnapshotProperties</b> method.

The provider is responsible for allocating and freeing the strings in the <a href="/windows/desktop/api/vss/ns-vss-vss_snapshot_prop">VSS_SNAPSHOT_PROP</a> structure.

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivsssoftwaresnapshotprovider">IVssSoftwareSnapshotProvider</a>



<a href="/windows/desktop/api/vsbackup/nf-vsbackup-vssfreesnapshotproperties">VssFreeSnapshotProperties</a>