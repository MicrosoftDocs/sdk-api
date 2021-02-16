---
UID: NF:vsmgmt.IVssDifferentialSoftwareSnapshotMgmt.QueryDiffAreasForSnapshot
title: IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForSnapshot (vsmgmt.h)
description: Queries shadow copy storage areas in use by the original volume associated with the input shadow copy.
helpviewer_keywords: ["IVssDifferentialSoftwareSnapshotMgmt interface [VSS]","QueryDiffAreasForSnapshot method","IVssDifferentialSoftwareSnapshotMgmt.QueryDiffAreasForSnapshot","IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForSnapshot","QueryDiffAreasForSnapshot","QueryDiffAreasForSnapshot method [VSS]","QueryDiffAreasForSnapshot method [VSS]","IVssDifferentialSoftwareSnapshotMgmt interface","base.ivssdifferentialsoftwaresnapshotmgmt_querydiffareasforsnapshot","vsmgmt/IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForSnapshot"]
old-location: base\ivssdifferentialsoftwaresnapshotmgmt_querydiffareasforsnapshot.htm
tech.root: base
ms.assetid: 1203d6de-b389-4349-a83c-5ee729add03c
ms.date: 12/05/2018
ms.keywords: IVssDifferentialSoftwareSnapshotMgmt interface [VSS],QueryDiffAreasForSnapshot method, IVssDifferentialSoftwareSnapshotMgmt.QueryDiffAreasForSnapshot, IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForSnapshot, QueryDiffAreasForSnapshot, QueryDiffAreasForSnapshot method [VSS], QueryDiffAreasForSnapshot method [VSS],IVssDifferentialSoftwareSnapshotMgmt interface, base.ivssdifferentialsoftwaresnapshotmgmt_querydiffareasforsnapshot, vsmgmt/IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForSnapshot
req.header: vsmgmt.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForSnapshot
 - vsmgmt/IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForSnapshot
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsMgmt.h
api_name:
 - IVssDifferentialSoftwareSnapshotMgmt.QueryDiffAreasForSnapshot
---

# IVssDifferentialSoftwareSnapshotMgmt::QueryDiffAreasForSnapshot


## -description

The 
    <b>QueryDiffAreasForSnapshot</b> 
    method queries shadow copy storage areas in use by the original volume associated with the input shadow copy.

## -parameters

### -param SnapshotId [in]

The <b>VSS_ID</b> of a shadow copy.

### -param ppEnum [out]

The address of an <a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssenummgmtobject">IVssEnumMgmtObject</a> interface 
      pointer, which is initialized on return. Callers must release the interface.

## -returns

This method can return one of these values.

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
Successfully queried the shadow copy storage areas.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Caller does not have sufficient backup privileges or is not an administrator.

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
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">
Provider error - the provider logged the error in the event log. For more information, see 
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

The returned <a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssenummgmtobject">IVssEnumMgmtObject</a> enumerator object 
    will contain <a href="/windows/desktop/api/vsmgmt/ns-vsmgmt-vss_diff_area_prop">VSS_DIFF_AREA_PROP</a> structures inside the 
    <a href="/openspecs/windows_protocols/ms-scmp/63b53947-2649-4eac-a883-498f77361396">VSS_MGMT_OBJECT_UNION</a> union inside the 
    <a href="/windows/desktop/api/vsmgmt/ns-vsmgmt-vss_mgmt_object_prop">VSS_MGMT_OBJECT_PROP</a> structure.

## -see-also

<a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt">IVssDifferentialSoftwareSnapshotMgmt</a>



<a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivssenummgmtobject">IVssEnumMgmtObject</a>

