---
UID: NF:vswriter.IVssComponentEx.GetRollForward
title: IVssComponentEx::GetRollForward
author: windows-sdk-content
description: Obtains the roll-forward operation type for a component and obtains the restore point for a partial roll-forward operation.
old-location: base\ivsscomponentex_getrollforward.htm
old-project: vss
ms.assetid: 4ba52c80-2229-4653-bd5b-85d9f11cd127
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetRollForward, GetRollForward method, GetRollForward method,IVssComponentEx interface, IVssComponentEx interface,GetRollForward method, IVssComponentEx.GetRollForward, IVssComponentEx::GetRollForward, base.ivsscomponentex_getrollforward, vswriter/IVssComponentEx::GetRollForward
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
 - IVssComponentEx.GetRollForward
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssComponentEx::GetRollForward


## -description


Obtains the roll-forward operation type for a component and obtains the restore point for a partial roll-forward operation.


## -parameters




### -param pRollType [out]

A <a href="https://msdn.microsoft.com/3a1f3123-659f-48e1-864d-d5abee64f819">VSS_ROLLFORWARD_TYPE</a> enumeration value indicating the type of roll-forward operation to be performed.


### -param pbstrPoint [out]

The address of a caller-allocated variable that receives a null-terminated wide character string specifying the roll-forward restore point.


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



The <b>GetRollForward</b> method can be called only during a restore operation.

If the call to <b>GetRollForward</b> is successful, the caller is responsible for freeing the string that  is returned in the <i>pRollType</i> parameter by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.

A writer indicates that it supports this method by setting the <b>VSS_BS_ROLLFORWARD_RESTORE</b> flag in its backup schema mask.

For more 
      information, see <a href="https://msdn.microsoft.com/364550a1-070a-4f7e-bd62-84672959dc21">Setting VSS Restore 
      Options</a>.




## -see-also




<a href="https://msdn.microsoft.com/9529284f-2150-4d32-af6c-178ba8681945">IVssBackupComponentsEx2::SetRollForward</a>



<a href="https://msdn.microsoft.com/b11f65b0-2de2-478b-88b6-4696a8da2419">IVssComponentEx</a>



<a href="https://msdn.microsoft.com/3541c8bd-2712-458b-9153-1fffe6bf5688">VSS_BACKUP_SCHEMA</a>



<a href="https://msdn.microsoft.com/3a1f3123-659f-48e1-864d-d5abee64f819">VSS_ROLLFORWARD_TYPE</a>
 

 

