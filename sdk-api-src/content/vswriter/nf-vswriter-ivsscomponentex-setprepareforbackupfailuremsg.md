---
UID: NF:vswriter.IVssComponentEx.SetPrepareForBackupFailureMsg
title: IVssComponentEx::SetPrepareForBackupFailureMsg
author: windows-sdk-content
description: Sets a PrepareForBackup failure message string for a component.
old-location: base\ivsscomponentex_setprepareforbackupfailuremsg.htm
old-project: vss
ms.assetid: b2c48c06-8bfc-431b-aab3-89ec9b30a9a0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IVssComponentEx interface,SetPrepareForBackupFailureMsg method, IVssComponentEx.SetPrepareForBackupFailureMsg, IVssComponentEx::SetPrepareForBackupFailureMsg, SetPrepareForBackupFailureMsg, SetPrepareForBackupFailureMsg method, SetPrepareForBackupFailureMsg method,IVssComponentEx interface, base.ivsscomponentex_setprepareforbackupfailuremsg, vswriter/IVssComponentEx::SetPrepareForBackupFailureMsg
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
 - IVssComponentEx.SetPrepareForBackupFailureMsg
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssComponentEx::SetPrepareForBackupFailureMsg


## -description


Sets a <a href="https://msdn.microsoft.com/en-us/library/Aa384664(v=VS.85).aspx">PrepareForBackup</a> failure message string for a component.

This method can only be called by a writer's <a href="https://msdn.microsoft.com/4e88d92b-48f3-42f9-bf66-61337a745902">CVssWriter::OnPrepareBackup</a> method.


## -parameters




### -param wszFailureMsg [in]

The address of a caller-allocated <b>NULL</b>-terminated wide character string containing the failure message that describes an error that occurred 
      while processing a <a href="https://msdn.microsoft.com/en-us/library/Aa384664(v=VS.85).aspx">PrepareForBackup</a> 
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
The failure message was successfully set.

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
This method was not called by a writer's <a href="https://msdn.microsoft.com/4e88d92b-48f3-42f9-bf66-61337a745902">CVssWriter::OnPrepareBackup</a> method.

</td>
</tr>
</table>
 




## -remarks



The failure message that is set by 
<b>SetPrepareForBackupFailureMsg</b> applies to all files in the component and any subcomponents.




## -see-also




<a href="https://msdn.microsoft.com/4e88d92b-48f3-42f9-bf66-61337a745902">CVssWriter::OnPrepareBackup</a>



<a href="https://msdn.microsoft.com/b11f65b0-2de2-478b-88b6-4696a8da2419">IVssComponentEx</a>



<a href="https://msdn.microsoft.com/b086ff8d-ff51-4550-887d-e7741e2469f2">IVssComponentEx::GetPrepareForBackupFailureMsg</a>
 

 

