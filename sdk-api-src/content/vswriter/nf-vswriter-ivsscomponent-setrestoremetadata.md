---
UID: NF:vswriter.IVssComponent.SetRestoreMetadata
title: IVssComponent::SetRestoreMetadata (vswriter.h)
description: The SetRestoreMetadata method sets writer-specific metadata for the current component.
helpviewer_keywords: ["IVssComponent interface [VSS]","SetRestoreMetadata method","IVssComponent.SetRestoreMetadata","IVssComponent::SetRestoreMetadata","SetRestoreMetadata","SetRestoreMetadata method [VSS]","SetRestoreMetadata method [VSS]","IVssComponent interface","_win32_ivsscomponent_setrestoremetadata","base.ivsscomponent_setrestoremetadata","vswriter/IVssComponent::SetRestoreMetadata"]
old-location: base\ivsscomponent_setrestoremetadata.htm
tech.root: base
ms.assetid: 2b329fa8-21ad-4de9-9857-52e14d51d429
ms.date: 12/05/2018
ms.keywords: IVssComponent interface [VSS],SetRestoreMetadata method, IVssComponent.SetRestoreMetadata, IVssComponent::SetRestoreMetadata, SetRestoreMetadata, SetRestoreMetadata method [VSS], SetRestoreMetadata method [VSS],IVssComponent interface, _win32_ivsscomponent_setrestoremetadata, base.ivsscomponent_setrestoremetadata, vswriter/IVssComponent::SetRestoreMetadata
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
 - IVssComponent::SetRestoreMetadata
 - vswriter/IVssComponent::SetRestoreMetadata
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
 - IVssComponent.SetRestoreMetadata
---

# IVssComponent::SetRestoreMetadata


## -description

The 
<b>SetRestoreMetadata</b> method sets writer-specific metadata for the current component.

Only a writer can call this method, and only in the context of implementing 
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onprerestore">CVssWriter::OnPreRestore</a>.

## -parameters

### -param wszRestoreMetadata [in]

A caller-allocated <b>NULL</b>-terminated wide character string containing the restore metadata for the component.

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
Successfully set the item.

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
<dt><b>VSS_E_OBJECT_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
Private metadata has already been written for this component.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
The method was called outside of the context of a writer handling a 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">PreRestore</a> event.

</td>
</tr>
</table>

## -remarks

<b>IVssComponent::SetRestoreMetadata</b> sets private, writer-specific metadata, which can be used by a writer during a restore operation.

The format need not conform to any VSS metadata specification.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getrestoremetadata">IVssComponent::GetRestoreMetadata</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-setbackupmetadata">IVssComponent::SetBackupMetadata</a>