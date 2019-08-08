---
UID: NF:vswriter.IVssComponentEx.GetAuthoritativeRestore
title: IVssComponentEx::GetAuthoritativeRestore (vswriter.h)
author: windows-sdk-content
description: Determines whether a requester has marked the restore of a component as authoritative for a replicated data store.
old-location: base\ivsscomponentex_getauthoritativerestore.htm
tech.root: VSS
ms.assetid: ca85cf27-b16c-4356-abb8-eb6474db637f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAuthoritativeRestore, GetAuthoritativeRestore method, GetAuthoritativeRestore method,IVssComponentEx interface, IVssComponentEx interface,GetAuthoritativeRestore method, IVssComponentEx.GetAuthoritativeRestore, IVssComponentEx::GetAuthoritativeRestore, base.ivsscomponentex_getauthoritativerestore, vswriter/IVssComponentEx::GetAuthoritativeRestore
ms.topic: method
f1_keywords:
- vswriter/IVssComponentEx.GetAuthoritativeRestore
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- VssApi.lib
- VssApi.dll
api_name:
- IVssComponentEx.GetAuthoritativeRestore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssComponentEx::GetAuthoritativeRestore


## -description


Determines whether a requester has marked the restore of a component as authoritative for a replicated data store.


## -parameters




### -param pbAuth [out]

The address of a caller-allocated variable that receives <b>true</b> if the restore is authoritative, or <b>false</b> otherwise.


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
The operation was successful.

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
</table>
 




## -remarks



A writer indicates that it supports authoritative restore by setting the <b>VSS_BS_AUTHORITATIVE_RESTORE</b> flag in its backup schema mask.

For more 
      information, see <a href="https://docs.microsoft.com/windows/desktop/VSS/setting-vss-restore-options">Setting VSS Restore 
      Options</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponentsex2-setauthoritativerestore">IVssBackupComponentsEx2::SetAuthoritativeRestore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nl-vswriter-ivsscomponentex">IVssComponentEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vss/ne-vss-vss_backup_schema">VSS_BACKUP_SCHEMA</a>
 

 

