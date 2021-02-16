---
UID: NF:vswriter.IVssComponent.GetBackupOptions
title: IVssComponent::GetBackupOptions (vswriter.h)
description: The GetBackupOptions method returns the backup options specified to the writer that manages the currently selected component or component set by a requester using IVssBackupComponents::SetBackupOptions.
helpviewer_keywords: ["GetBackupOptions","GetBackupOptions method [VSS]","GetBackupOptions method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","GetBackupOptions method","IVssComponent.GetBackupOptions","IVssComponent::GetBackupOptions","_win32_ivsscomponent_getbackupoptions","base.ivsscomponent_getbackupoptions","vswriter/IVssComponent::GetBackupOptions"]
old-location: base\ivsscomponent_getbackupoptions.htm
tech.root: base
ms.assetid: 54182058-5dbb-4eda-959a-fa1921a27302
ms.date: 12/05/2018
ms.keywords: GetBackupOptions, GetBackupOptions method [VSS], GetBackupOptions method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetBackupOptions method, IVssComponent.GetBackupOptions, IVssComponent::GetBackupOptions, _win32_ivsscomponent_getbackupoptions, base.ivsscomponent_getbackupoptions, vswriter/IVssComponent::GetBackupOptions
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
 - IVssComponent::GetBackupOptions
 - vswriter/IVssComponent::GetBackupOptions
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
 - IVssComponent.GetBackupOptions
---

# IVssComponent::GetBackupOptions


## -description

The 
<b>GetBackupOptions</b> method returns the backup options specified to the writer that manages the currently selected component or component set by a requester using 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions">IVssBackupComponents::SetBackupOptions</a>.

Either a writer or a requester can call this method.

## -parameters

### -param pbstrBackupOptions [out]

The address of a caller-allocated variable that receives a string containing the backup options for the current writer.

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
No backup options have been specified for this component.

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

If no backup options have been set, S_FALSE is returned.

If the call to <b>GetBackupOptions</b> is successful, the caller is responsible for freeing the string that  is returned in the <i>pbstrBackupOptions</i> parameter by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions">IVssBackupComponents::SetBackupOptions</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getrestoreoptions">IVssComponent::GetRestoreOptions</a>