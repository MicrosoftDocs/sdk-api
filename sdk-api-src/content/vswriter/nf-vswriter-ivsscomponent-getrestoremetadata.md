---
UID: NF:vswriter.IVssComponent.GetRestoreMetadata
title: IVssComponent::GetRestoreMetadata (vswriter.h)
description: The GetRestoreMetadata method retrieves private, writer-specific restore metadata that might have been set during a PreRestore event by CVssWriter::OnPreRestore using IVssComponent::SetRestoreMetadata.
helpviewer_keywords: ["GetRestoreMetadata","GetRestoreMetadata method [VSS]","GetRestoreMetadata method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","GetRestoreMetadata method","IVssComponent.GetRestoreMetadata","IVssComponent::GetRestoreMetadata","_win32_ivsscomponent_getrestoremetadata","base.ivsscomponent_getrestoremetadata","vswriter/IVssComponent::GetRestoreMetadata"]
old-location: base\ivsscomponent_getrestoremetadata.htm
tech.root: base
ms.assetid: 1b53c523-a105-4507-89f3-1f746aa86204
ms.date: 12/05/2018
ms.keywords: GetRestoreMetadata, GetRestoreMetadata method [VSS], GetRestoreMetadata method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetRestoreMetadata method, IVssComponent.GetRestoreMetadata, IVssComponent::GetRestoreMetadata, _win32_ivsscomponent_getrestoremetadata, base.ivsscomponent_getrestoremetadata, vswriter/IVssComponent::GetRestoreMetadata
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
 - IVssComponent::GetRestoreMetadata
 - vswriter/IVssComponent::GetRestoreMetadata
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
 - IVssComponent.GetRestoreMetadata
---

# IVssComponent::GetRestoreMetadata


## -description

The <b>GetRestoreMetadata</b> method retrieves
    private, writer-specific restore metadata that might have been set during a 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">PreRestore</a> event by 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onprerestore">CVssWriter::OnPreRestore</a> using 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-setrestoremetadata">IVssComponent::SetRestoreMetadata</a>.
   

Only a writer can call this method.

## -parameters

### -param pbstrRestoreMetadata [out]

A string containing the restore metadata.

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
The XML document is not valid. Check the event log for details. For more
        information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.
       

</td>
</tr>
</table>

## -remarks

This method can be called at any time depending on the logic of a given writer.

The caller should free the memory held by the <i>pbstrRestoreMetadata</i> parameter by calling 
    <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a>.
   

If no backup metadata has been set, 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getbackupmetadata">GetBackupMetadata</a> returns S_FALSE.
   

A writer setting the restore method to VSS_RME_RESTORE_TO_ALTERNATE_LOCATION without defining an alternate
    location mapping constitutes a writer error.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>