---
UID: NF:vswriter.IVssComponentEx.GetAuthoritativeRestore
title: IVssComponentEx::GetAuthoritativeRestore method
author: windows-driver-content
description: Determines whether a requester has marked the restore of a component as authoritative for a replicated data store.
old-location: base\ivsscomponentex_getauthoritativerestore.htm
old-project: VSS
ms.assetid: ca85cf27-b16c-4356-abb8-eb6474db637f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetAuthoritativeRestore method, GetAuthoritativeRestore method, IVssComponentEx interface, GetAuthoritativeRestore,IVssComponentEx.GetAuthoritativeRestore, IVssComponentEx, IVssComponentEx interface, GetAuthoritativeRestore method, IVssComponentEx::GetAuthoritativeRestore, base.ivsscomponentex_getauthoritativerestore, vswriter/IVssComponentEx::GetAuthoritativeRestore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	IVssComponentEx.GetAuthoritativeRestore
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssComponentEx::GetAuthoritativeRestore method


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
      information, see <a href="https://msdn.microsoft.com/364550a1-070a-4f7e-bd62-84672959dc21">Setting VSS Restore 
      Options</a>.




## -see-also




<a href="https://msdn.microsoft.com/3725a282-2df8-4a0a-a1bf-a73c2b259cbf">IVssBackupComponentsEx2::SetAuthoritativeRestore</a>



<a href="https://msdn.microsoft.com/b11f65b0-2de2-478b-88b6-4696a8da2419">IVssComponentEx</a>



<a href="https://msdn.microsoft.com/3541c8bd-2712-458b-9153-1fffe6bf5688">VSS_BACKUP_SCHEMA</a>
 

 

