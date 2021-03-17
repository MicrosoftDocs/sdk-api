---
UID: NF:vswriter.IVssComponent.SetPreRestoreFailureMsg
title: IVssComponent::SetPreRestoreFailureMsg (vswriter.h)
description: The SetPreRestoreFailureMsg method is used to create a message describing a failure in processing a PreRestore event.
helpviewer_keywords: ["IVssComponent interface [VSS]","SetPreRestoreFailureMsg method","IVssComponent.SetPreRestoreFailureMsg","IVssComponent::SetPreRestoreFailureMsg","SetPreRestoreFailureMsg","SetPreRestoreFailureMsg method [VSS]","SetPreRestoreFailureMsg method [VSS]","IVssComponent interface","_win32_ivsscomponent_setprerestorefailuremsg","base.ivsscomponent_setprerestorefailuremsg","vswriter/IVssComponent::SetPreRestoreFailureMsg"]
old-location: base\ivsscomponent_setprerestorefailuremsg.htm
tech.root: base
ms.assetid: 5b273cba-9878-4494-81ef-af1367f1e0a5
ms.date: 12/05/2018
ms.keywords: IVssComponent interface [VSS],SetPreRestoreFailureMsg method, IVssComponent.SetPreRestoreFailureMsg, IVssComponent::SetPreRestoreFailureMsg, SetPreRestoreFailureMsg, SetPreRestoreFailureMsg method [VSS], SetPreRestoreFailureMsg method [VSS],IVssComponent interface, _win32_ivsscomponent_setprerestorefailuremsg, base.ivsscomponent_setprerestorefailuremsg, vswriter/IVssComponent::SetPreRestoreFailureMsg
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
 - IVssComponent::SetPreRestoreFailureMsg
 - vswriter/IVssComponent::SetPreRestoreFailureMsg
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
 - IVssComponent.SetPreRestoreFailureMsg
---

# IVssComponent::SetPreRestoreFailureMsg


## -description

The <b>SetPreRestoreFailureMsg</b> 
    method is used to create a message describing a failure in processing a 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">PreRestore</a> event.

Only a writer can call this method, and only during a restore operation.

## -parameters

### -param wszPreRestoreFailureMsg [in]

A caller-allocated <b>NULL</b>-terminated wide character string containing the failure message describing an error that occurred 
      while processing a <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">PreRestore</a> 
      event.

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
Successfully set the failure message.

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
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
The caller is not in the correct state (either backup or restore) for the operation.

</td>
</tr>
</table>

## -remarks

The failure message set by 
    <b>SetPreRestoreFailureMsg</b> applies to 
    all files in the component and any nonselectable subcomponents.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg">IVssComponent::GetPostRestoreFailureMsg</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg">IVssComponent::GetPreRestoreFailureMsg</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg">IVssComponent::SetPostRestoreFailureMsg</a>