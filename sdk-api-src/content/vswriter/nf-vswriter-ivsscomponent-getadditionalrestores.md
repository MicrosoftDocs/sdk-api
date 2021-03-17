---
UID: NF:vswriter.IVssComponent.GetAdditionalRestores
title: IVssComponent::GetAdditionalRestores (vswriter.h)
description: The GetAdditionalRestores method is used by a writer during incremental or differential restore operations to determine whether a given component will require additional restore operations to completely retrieve it.
helpviewer_keywords: ["GetAdditionalRestores","GetAdditionalRestores method [VSS]","GetAdditionalRestores method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","GetAdditionalRestores method","IVssComponent.GetAdditionalRestores","IVssComponent::GetAdditionalRestores","_win32_ivsscomponent_getadditionalrestores","base.ivsscomponent_getadditionalrestores","vswriter/IVssComponent::GetAdditionalRestores"]
old-location: base\ivsscomponent_getadditionalrestores.htm
tech.root: base
ms.assetid: f398a88a-6572-4d0b-a241-37cc0e9e99a0
ms.date: 12/05/2018
ms.keywords: GetAdditionalRestores, GetAdditionalRestores method [VSS], GetAdditionalRestores method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetAdditionalRestores method, IVssComponent.GetAdditionalRestores, IVssComponent::GetAdditionalRestores, _win32_ivsscomponent_getadditionalrestores, base.ivsscomponent_getadditionalrestores, vswriter/IVssComponent::GetAdditionalRestores
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
 - IVssComponent::GetAdditionalRestores
 - vswriter/IVssComponent::GetAdditionalRestores
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
 - IVssComponent.GetAdditionalRestores
---

# IVssComponent::GetAdditionalRestores


## -description

The 
<b>GetAdditionalRestores</b> method is used by a writer during incremental or differential restore operations to determine whether a given component will require additional restore operations to completely retrieve it.

Either a writer or a requester can call this method.

## -parameters

### -param pbAdditionalRestores [out]

The address of a caller-allocated variable that receives <b>true</b> if additional restores will occur for the current component, or <b>false</b> otherwise.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified attribute does not have a value.

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
</table>

## -remarks

The value returned by 
<b>GetAdditionalRestores</b> will be false, unless during a restore operation a requester calls 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores">IVssBackupComponents::SetAdditionalRestores</a>.

<b>GetAdditionalRestores</b> should be used to check if it is necessary to use more than one backup set to completely restore a component. A component might first be retrieved by restoring data from a full backup, and then updating that data from one or more subsequent incremental or differential backups.

The 
<b>GetAdditionalRestores</b> method is typically used by writers that support an explicit recovery mechanism as part of their 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-postrestore">PostRestore</a> event handler (<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore">CVssWriter::OnPostRestore</a>)—for instance, the Exchange Server, and database applications such as SQL Server. For these applications, it is often not possible to perform additional differential, incremental, or log restores after such a recovery is performed.

Therefore, if 
<b>GetAdditionalRestores</b> returns <b>true</b> for a component, such a writer should not execute its explicit recovery mechanism and should expect that additional differential, incremental, or log restores will be done.

When 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores">SetAdditionalRestores</a> returns <b>false</b>, then after the restore has finished, when handling the 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-postrestore">PostRestore</a> event, the writer can complete its recovery operation and be brought back online.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>