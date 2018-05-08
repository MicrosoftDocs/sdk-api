---
UID: NF:vsbackup.IVssBackupComponents.SetBackupSucceeded
title: IVssBackupComponents::SetBackupSucceeded
author: windows-driver-content
description: The SetBackupSucceeded method indicates whether the backup of the specified component of a specific writer was successful.
old-location: base\ivssbackupcomponents_setbackupsucceeded.htm
old-project: VSS
ms.assetid: 5565183d-f374-4796-a399-b008041afdd2
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: IVssBackupComponents interface [VSS],SetBackupSucceeded method, IVssBackupComponents.SetBackupSucceeded, IVssBackupComponents::SetBackupSucceeded, SetBackupSucceeded, SetBackupSucceeded method [VSS], SetBackupSucceeded method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_setbackupsucceeded, base.ivssbackupcomponents_setbackupsucceeded, vsbackup/IVssBackupComponents::SetBackupSucceeded
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IVssBackupComponents.SetBackupSucceeded
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssBackupComponents::SetBackupSucceeded


## -description


The 
<b>SetBackupSucceeded</b> method indicates whether the backup of the specified component of a specific writer was successful.


## -parameters




### -param instanceId [in]

Globally unique identifier (GUID) of the writer instance.


### -param writerId [in]

Globally unique identifier (GUID) of the writer class.


### -param ct




### -param wszLogicalPath [in]

<b>Null</b>-terminated wide character string containing the logical path of the component. 


For more information, see <a href="https://msdn.microsoft.com/663c8ca9-8f5b-48bd-af2d-b2d90de9e492">Logical Pathing of Components</a>.

The value of the string containing the logical path used here should be the same as was used when the component was added to the backup set using 
<a href="https://msdn.microsoft.com/50cb0b16-9ed3-4496-962a-9c845c10986c">IVssBackupComponents::AddComponent</a>.

The logical path can be <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-<b>NULL</b> logical path.


### -param wszComponentName [in]

<b>Null</b>-terminated wide character string containing the name of the component. 




The string cannot be <b>NULL</b> and should contain the same component name as was used when the component was added to the backup set using 
<a href="https://msdn.microsoft.com/50cb0b16-9ed3-4496-962a-9c845c10986c">IVssBackupComponents::AddComponent</a>.


### -param bSucceded






#### - bSucceeded [in]

Set this parameter to <b>true</b> if the component was successfully backed up, or <b>false</b> otherwise.


#### - componentType [in]

Type of the component. See 
<a href="https://msdn.microsoft.com/ba3b726c-448a-46c0-8fa5-5793497aa385">VSS_COMPONENT_TYPE</a> for the possible values.


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
Successfully set the backup succeeded state.

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
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The backup component does not exist.

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



When working in component mode (when 
<a href="https://msdn.microsoft.com/18a1295d-b763-477b-bda2-baf8a878bf46">IVssBackupComponents::SetBackupState</a> is called with its select components argument set to <b>true</b>), writers check the state of each components backup using 
<a href="https://msdn.microsoft.com/9b2dce08-a4ab-4e55-aeef-819f71ddf9d2">IVssComponent::GetBackupSucceeded</a>. Therefore, a well-behaved backup application (requester) must call 
<b>SetBackupSucceeded</b> after each component has been processed and prior to calling 
<a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">IVssBackupComponents::BackupComplete</a>.

Do not call this method if the call to <a href="https://msdn.microsoft.com/3cc6c375-8a24-4af3-b4ad-5a695cc2645c">IVssBackupComponents::DoSnapshotSet</a> failed.  For more information about how requesters use  <b>DoSnapshotSet</b>, <b>SetBackupSucceeded</b>, and <a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">BackupComplete</a> in a backup operation, see <a href="https://msdn.microsoft.com/e6b082af-719b-4426-8217-0fc940f5884d">Overview of Pre-Backup Tasks</a> and <a href="https://msdn.microsoft.com/187f26f2-f191-4703-9bde-3357f1ceef0c">Overview of Actual Backup Of Files</a>.




## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">IVssBackupComponents::BackupComplete</a>



<a href="https://msdn.microsoft.com/18a1295d-b763-477b-bda2-baf8a878bf46">IVssBackupComponents::SetBackupState</a>



<a href="https://msdn.microsoft.com/ba3b726c-448a-46c0-8fa5-5793497aa385">VSS_COMPONENT_TYPE</a>
 

 

