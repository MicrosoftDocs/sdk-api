---
UID: NF:vsbackup.IVssBackupComponents.GetSnapshotProperties
title: IVssBackupComponents::GetSnapshotProperties
author: windows-sdk-content
description: The GetSnapshotProperties method gets the properties of the specified shadow copy.
old-location: base\ivssbackupcomponents_getsnapshotproperties.htm
old-project: vss
ms.assetid: a4e2f9f3-7dee-4324-a48a-6de2a32eabf7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetSnapshotProperties, GetSnapshotProperties method [VSS], GetSnapshotProperties method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],GetSnapshotProperties method, IVssBackupComponents.GetSnapshotProperties, IVssBackupComponents::GetSnapshotProperties, _win32_ivssbackupcomponents_getsnapshotproperties, base.ivssbackupcomponents_getsnapshotproperties, vsbackup/IVssBackupComponents::GetSnapshotProperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.redist: 
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
tech.root: 
req.typenames: AMVPSIZE, *LPAMVPSIZE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssBackupComponents.GetSnapshotProperties
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssBackupComponents::GetSnapshotProperties


## -description


The <b>GetSnapshotProperties</b> 
    method gets the properties of the specified shadow copy.
   


## -parameters




### -param SnapshotId [in]

The identifier of the shadow copy of a volume as returned by 
      <a href="https://msdn.microsoft.com/6c20e386-7cd8-45d9-92d6-96d0a458db50">IVssBackupComponents::AddToSnapshotSet</a>.
     


### -param pProp [out]

The address of a caller-allocated <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure that receives 
      the shadow copy properties.
      The software provider is responsible for setting the members of this structure. The software provider allocates memory for all string members  that it sets in the structure. When the structure is no longer needed, the software provider is responsible for freeing these strings by calling the <a href="https://msdn.microsoft.com/d5b5883b-03d5-4a83-af2e-f4d22e26ee82">VssFreeSnapshotProperties</a> function.


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
Successfully returned the shadow copy properties.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient backup privileges or is not an administrator.

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
The backup components object is not initialized, this method has been called during a restore operation, or 
        this method has not been called within the correct sequence.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified shadow copy does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
</dl>
</td>
<td width="60%">
Expected provider error. The provider logged the error in the event log. For more information, see 
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED_PROVIDER_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Unexpected provider error. The error code is logged in the error log. For more information, see 
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event 
        and Error Handling Under VSS</a>.
       

</td>
</tr>
</table>
 




## -remarks



The caller should set the contents of the <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure to zero before calling the <b>GetSnapshotProperties</b> method.

The provider is responsible for allocating and freeing the strings in the <a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/6c20e386-7cd8-45d9-92d6-96d0a458db50">IVssBackupComponents::AddToSnapshotSet</a>



<a href="https://msdn.microsoft.com/6a0a6228-2131-48a6-8d18-9491969d265b">IVssBackupComponents::StartSnapshotSet</a>



<a href="https://msdn.microsoft.com/e64b36d6-4f10-42bd-9ad4-00aba90e9715">VSS_ID</a>



<a href="https://msdn.microsoft.com/070ec204-e751-4ebf-8f99-3c415f203cb2">VSS_SNAPSHOT_PROP</a>



<a href="https://msdn.microsoft.com/d5b5883b-03d5-4a83-af2e-f4d22e26ee82">VssFreeSnapshotProperties</a>
 

 

