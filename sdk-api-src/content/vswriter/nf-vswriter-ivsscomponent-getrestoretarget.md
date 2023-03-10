---
UID: NF:vswriter.IVssComponent.GetRestoreTarget
title: IVssComponent::GetRestoreTarget (vswriter.h)
description: The GetRestoreTarget method returns the restore target (in terms of the VSS_RESTORE_TARGET enumeration) for the current component.
helpviewer_keywords: ["GetRestoreTarget","GetRestoreTarget method [VSS]","GetRestoreTarget method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","GetRestoreTarget method","IVssComponent.GetRestoreTarget","IVssComponent::GetRestoreTarget","_win32_ivsscomponent_getrestoretarget","base.ivsscomponent_getrestoretarget","vswriter/IVssComponent::GetRestoreTarget"]
old-location: base\ivsscomponent_getrestoretarget.htm
tech.root: base
ms.assetid: e2361e38-8757-4a29-bbaf-7f659d1095d9
ms.date: 12/05/2018
ms.keywords: GetRestoreTarget, GetRestoreTarget method [VSS], GetRestoreTarget method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetRestoreTarget method, IVssComponent.GetRestoreTarget, IVssComponent::GetRestoreTarget, _win32_ivsscomponent_getrestoretarget, base.ivsscomponent_getrestoretarget, vswriter/IVssComponent::GetRestoreTarget
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IVssComponent::GetRestoreTarget
 - vswriter/IVssComponent::GetRestoreTarget
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
 - IVssComponent.GetRestoreTarget
---

# IVssComponent::GetRestoreTarget


## -description

The 
<b>GetRestoreTarget</b> method returns the restore target (in terms of the 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_restore_target">VSS_RESTORE_TARGET</a> enumeration) for the current component.

Either a writer or a requester can call this method. It can be called only during a restore operation.

## -parameters

### -param pTarget [out]

The address of a caller-allocated variable that receives a 
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_restore_target">VSS_RESTORE_TARGET</a> enumeration value that specifies the restore target.

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
Successfully returned the attribute value.

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
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more information, see 
<a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified item was not found.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>