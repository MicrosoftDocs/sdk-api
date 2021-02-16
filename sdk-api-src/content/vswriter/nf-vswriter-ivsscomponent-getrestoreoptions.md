---
UID: NF:vswriter.IVssComponent.GetRestoreOptions
title: IVssComponent::GetRestoreOptions (vswriter.h)
description: The GetRestoreOptions method gets the restore options specified to the current writer by a requester using IVssBackupComponents::SetRestoreOptions.
helpviewer_keywords: ["GetRestoreOptions","GetRestoreOptions method [VSS]","GetRestoreOptions method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","GetRestoreOptions method","IVssComponent.GetRestoreOptions","IVssComponent::GetRestoreOptions","_win32_ivsscomponent_getrestoreoptions","base.ivsscomponent_getrestoreoptions","vswriter/IVssComponent::GetRestoreOptions"]
old-location: base\ivsscomponent_getrestoreoptions.htm
tech.root: base
ms.assetid: 818fd713-1b41-4abd-aca4-c74383fa3594
ms.date: 12/05/2018
ms.keywords: GetRestoreOptions, GetRestoreOptions method [VSS], GetRestoreOptions method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetRestoreOptions method, IVssComponent.GetRestoreOptions, IVssComponent::GetRestoreOptions, _win32_ivsscomponent_getrestoreoptions, base.ivsscomponent_getrestoreoptions, vswriter/IVssComponent::GetRestoreOptions
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
 - IVssComponent::GetRestoreOptions
 - vswriter/IVssComponent::GetRestoreOptions
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
 - IVssComponent.GetRestoreOptions
---

# IVssComponent::GetRestoreOptions


## -description

The 
<b>GetRestoreOptions</b> method gets the restore options specified to the current writer by a requester using 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions">IVssBackupComponents::SetRestoreOptions</a>.

Either a writer or a requester can call this method.

## -parameters

### -param pbstrRestoreOptions [out]

String containing the restore options of the writer.

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
No restore options have been specified.

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

The caller should free the memory held by the <i>pbstrRestoreOptions</i> parameter by calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.

If no restore options have been set, S_FALSE is returned.

## -see-also

<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions">IVssBackupComponents::SetRestoreOptions</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getbackupoptions">IVssComponent::GetBackupOptions</a>