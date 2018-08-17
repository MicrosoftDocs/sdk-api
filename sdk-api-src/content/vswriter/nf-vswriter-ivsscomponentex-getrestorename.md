---
UID: NF:vswriter.IVssComponentEx.GetRestoreName
title: IVssComponentEx::GetRestoreName
author: windows-sdk-content
description: Obtains the logical name assigned to a component that is being restored.
old-location: base\ivsscomponentex_getrestorename.htm
old-project: vss
ms.assetid: a544bcc1-6a42-4cda-824c-2b027b8a4a6f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetRestoreName, GetRestoreName method, GetRestoreName method,IVssComponentEx interface, IVssComponentEx interface,GetRestoreName method, IVssComponentEx.GetRestoreName, IVssComponentEx::GetRestoreName, base.ivsscomponentex_getrestorename, vswriter/IVssComponentEx::GetRestoreName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.redist: 
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
tech.root: 
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssComponentEx.GetRestoreName
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssComponentEx::GetRestoreName


## -description


Obtains the logical name assigned to a component that is being restored.


## -parameters




### -param pbstrName [out]

The address of a caller-allocated variable that receives a null-terminated wide character string containing the restore name for the component.


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



The <a href="https://msdn.microsoft.com/a8334b28-9328-49f4-bf92-f43c556781bf">GetRestoreName</a> method can only be called during a restore operation.

If the call to <a href="https://msdn.microsoft.com/a8334b28-9328-49f4-bf92-f43c556781bf">GetRestoreName</a> is successful, the caller is responsible for freeing the string that  is returned in the <i>pbstrName</i> parameter by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.

A writer indicates that it supports this method by setting the <b>VSS_BS_RESTORE_RENAME</b> flag in its backup schema mask.

For more 
      information, see <a href="https://msdn.microsoft.com/364550a1-070a-4f7e-bd62-84672959dc21">Setting VSS Restore 
      Options</a>.




## -see-also




<a href="https://msdn.microsoft.com/a8334b28-9328-49f4-bf92-f43c556781bf">IVssBackupComponentsEx2::SetRestoreName</a>



<a href="https://msdn.microsoft.com/b11f65b0-2de2-478b-88b6-4696a8da2419">IVssComponentEx</a>



<a href="https://msdn.microsoft.com/3541c8bd-2712-458b-9153-1fffe6bf5688">VSS_BACKUP_SCHEMA</a>
 

 

