---
UID: NF:vsbackup.IVssBackupComponents.SetBackupState
title: IVssBackupComponents::SetBackupState
author: windows-sdk-content
description: The SetBackupState method defines an overall configuration for a backup operation.
old-location: base\ivssbackupcomponents_setbackupstate.htm
old-project: VSS
ms.assetid: 18a1295d-b763-477b-bda2-baf8a878bf46
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IVssBackupComponents interface [VSS],SetBackupState method, IVssBackupComponents.SetBackupState, IVssBackupComponents::SetBackupState, SetBackupState, SetBackupState method [VSS], SetBackupState method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_setbackupstate, base.ivssbackupcomponents_setbackupstate, vsbackup/IVssBackupComponents::SetBackupState
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	IVssBackupComponents.SetBackupState
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssBackupComponents::SetBackupState


## -description


The 
<b>SetBackupState</b> method defines an overall configuration for a backup operation.


## -parameters




### -param bSelectComponents [in]

Indicates whether a backup or restore operation will be in component mode. 




Operation in component mode supports selectively backing up designated individual components (which can allow their exclusion), or only supports backing up all files and components on a volume.

The Boolean is <b>true</b> if the operation will be conducted in component mode and <b>false</b> if not.


### -param bBackupBootableSystemState [in]

Indicates whether a bootable system state backup is being performed.


### -param backupType [in]

A 
<a href="https://msdn.microsoft.com/82934737-0d80-4b5d-a1fa-1ba38e446504">VSS_BACKUP_TYPE</a> enumeration value indicating the type of backup to be performed.


### -param bPartialFileSupport [in]

Optional. If the value of this parameter is <b>true</b>, partial file support is enabled. The default value for this argument is <b>false</b>.


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
Successfully set the backup state.

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
The backup components object is not initialized, this method has been called during a restore operation, or this method has not been called within the correct sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more information, see 
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
</table>
 




## -remarks



Applications must call 
<b>SetBackupState</b> prior to calling 
<a href="https://msdn.microsoft.com/46ce8282-a434-4b0b-b66e-40810052b34b">IVssBackupComponents::PrepareForBackup</a>.




## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/82934737-0d80-4b5d-a1fa-1ba38e446504">VSS_BACKUP_TYPE</a>
 

 

