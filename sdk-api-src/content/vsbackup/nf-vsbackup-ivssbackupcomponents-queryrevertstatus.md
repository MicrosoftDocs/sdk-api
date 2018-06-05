---
UID: NF:vsbackup.IVssBackupComponents.QueryRevertStatus
title: IVssBackupComponents::QueryRevertStatus
author: windows-sdk-content
description: Returns an IVssAsync interface pointer that can be used to determine the status of the revert operation.
old-location: base\ivssbackupcomponents_queryrevertstatus.htm
old-project: VSS
ms.assetid: f2e97723-98cb-401c-ab35-20c004f0a73d
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IVssBackupComponents interface [VSS],QueryRevertStatus method, IVssBackupComponents.QueryRevertStatus, IVssBackupComponents::QueryRevertStatus, QueryRevertStatus, QueryRevertStatus method [VSS], QueryRevertStatus method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_queryrevertstatus, base.ivssbackupcomponents_queryrevertstatus, vsbackup/IVssBackupComponents::QueryRevertStatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: AMVPSIZE, *LPAMVPSIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	IVssBackupComponents.QueryRevertStatus
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssBackupComponents::QueryRevertStatus


## -description


The <b>QueryRevertStatus</b> method 
   returns an <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> interface pointer that can be used 
   to determine the status of the revert operation.


## -parameters




### -param pwszVolume [in]

Null-terminated wide character string containing the name of the volume. The name must be in one of the following formats and must include a trailing backslash (\): 
      

<ul>
<li>The path of a mounted folder, for example, Y:\MountX\</li>
<li>A drive letter, for example, D:\</li>
<li>A volume GUID path of the form \\?\<i>Volume</i>{<i>GUID</i>}\ (where <i>GUID</i> identifies the volume)</li>
</ul>

### -param ppAsync [out]

Pointer to a location that will receive an <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> 
      interface pointer that can be used to retrieve the status of the revert process. When the operation is complete, the caller must release the interface pointer by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_ACCESSDENIED</b></b></dt>
</dl>
</td>
<td width="60%">
The calling process has insufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_FAIL</b></b></dt>
</dl>
</td>
<td width="60%">
There is an internal error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_INVALIDARG</b></b></dt>
</dl>
</td>
<td width="60%">
One of the parameters passed is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_NOTIMPL</b></b></dt>
</dl>
</td>
<td width="60%">
The provider for the volume does not support revert operations.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_OUTOFMEMORY</b></b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_POINTER</b></b></dt>
</dl>
</td>
<td width="60%">
One of the required pointer parameters is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VSS_E_OBJECT_NOT_FOUND</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszVolume</i> parameter is not a valid volume.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VSS_E_VOLUME_NOT_SUPPORTED</b></b></dt>
</dl>
</td>
<td width="60%">
Revert is not supported on this volume.

</td>
</tr>
</table>
 




## -remarks



The revert operation will continue even if the computer is rebooted, and cannot be canceled or undone, except 
    by restoring a backup created using another method. The 
    <a href="https://msdn.microsoft.com/85fb3ae8-dc09-4f6f-a96b-e4dc046ff48a">QueryStatus</a> method on the returned  
    <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> interface cannot return 
    <b>VSS_S_ASYNC_CANCELLED</b> as the revert operation cannot be canceled after it has 
    started.




## -see-also




<a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a>



<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/9976195e-3448-4b0e-82b2-1ae061c75b17">IVssBackupComponents::RevertToSnapshot</a>
 

 

