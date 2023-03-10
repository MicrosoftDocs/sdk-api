---
UID: NF:vswriter.IVssComponent.GetBackupMetadata
title: IVssComponent::GetBackupMetadata (vswriter.h)
description: The GetBackupMetadata method retrieves private, writer-specific backup metadata that might have been set during a PrepareForBackup event by CVssWriter::OnPrepareBackup using IVssComponent::SetBackupMetadata.
helpviewer_keywords: ["GetBackupMetadata","GetBackupMetadata method [VSS]","GetBackupMetadata method [VSS]","IVssComponent interface","IVssComponent interface [VSS]","GetBackupMetadata method","IVssComponent.GetBackupMetadata","IVssComponent::GetBackupMetadata","_win32_ivsscomponent_getbackupmetadata","base.ivsscomponent_getbackupmetadata","vswriter/IVssComponent::GetBackupMetadata"]
old-location: base\ivsscomponent_getbackupmetadata.htm
tech.root: base
ms.assetid: 638b8909-0aef-4066-ade7-4ee6d96b309e
ms.date: 12/05/2018
ms.keywords: GetBackupMetadata, GetBackupMetadata method [VSS], GetBackupMetadata method [VSS],IVssComponent interface, IVssComponent interface [VSS],GetBackupMetadata method, IVssComponent.GetBackupMetadata, IVssComponent::GetBackupMetadata, _win32_ivsscomponent_getbackupmetadata, base.ivsscomponent_getbackupmetadata, vswriter/IVssComponent::GetBackupMetadata
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
 - IVssComponent::GetBackupMetadata
 - vswriter/IVssComponent::GetBackupMetadata
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
 - IVssComponent.GetBackupMetadata
---

# IVssComponent::GetBackupMetadata


## -description

The <b>GetBackupMetadata</b> method retrieves 
    private, writer-specific backup metadata that might have been set during a 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup">PrepareForBackup</a> event by 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">CVssWriter::OnPrepareBackup</a> using 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-setbackupmetadata">IVssComponent::SetBackupMetadata</a>.
   

Only a writer can call this method.

## -parameters

### -param pbstrData [out]

The address of a caller-allocated variable that receives a string containing the backup metadata that was added during an 
      <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">OnPrepareBackup</a> event.

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
There is no backup metadata associated with this component.

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

If no backup metadata has been set, 
    <b>GetBackupMetadata</b> returns S_FALSE.
   

If the call to <b>GetBackupMetadata</b> is successful, the caller is responsible for freeing the string that  is returned in the <i>pbstrMetadata</i> parameter by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-setbackupmetadata">IVssComponent::SetBackupMetadata</a>