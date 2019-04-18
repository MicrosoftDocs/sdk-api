---
UID: NL:vsbackup.IVssBackupComponents
title: IVssBackupComponents (vsbackup.h)
author: windows-sdk-content
description: The IVssBackupComponents interface is used by a requester to poll writers about file status and to run backup/restore operations.
old-location: base\ivssbackupcomponents.htm
tech.root: VSS
ms.assetid: fe1220c7-11e5-4872-b7a9-61558f7c75c0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents, IVssBackupComponents interface [VSS], IVssBackupComponents interface [VSS],described, _win32_ivssbackupcomponents, base.ivssbackupcomponents, vsbackup/IVssBackupComponents
ms.topic: class
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
 - IVssBackupComponents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssBackupComponents class


## -description


The <b>IVssBackupComponents</b> interface is used by a 
    requester to poll writers about file status and to run backup/restore operations.

Applications obtain an instance of the 
    <b>IVssBackupComponents</b> interface by calling 
    <a href="https://msdn.microsoft.com/5531e57a-49e0-42e9-abf0-e8a4849ccac6">CreateVssBackupComponents</a>.

An <b>IVssBackupComponents</b> object can be used for 
    only a single backup, restore, or <a href="https://msdn.microsoft.com/3f79bf84-c7b9-4291-ae3b-7061fe3199e9">Query</a> operation.

After the backup, restore, or <a href="https://msdn.microsoft.com/3f79bf84-c7b9-4291-ae3b-7061fe3199e9">Query</a> operation has either successfully finished or been explicitly terminated, a requester must 
    release the <b>IVssBackupComponents</b> object by calling 
    <b>IVssBackupComponents::Release</b>. An 
    <b>IVssBackupComponents</b> object must not be reused. For example, you cannot perform a backup or restore operation with the same <b>IVssBackupComponents</b> object that you have already used for a <b>Query</b> operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssBackupComponents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVssBackupComponents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssBackupComponents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e854ab83-9a1a-4660-8a3e-37747b1b7d8c">AbortBackup</a>
</td>
<td align="left" width="63%">
Terminates the current backup.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/349ec124-f3f5-4142-8600-8d9f508c9bb2">AddAlternativeLocationMapping</a>
</td>
<td align="left" width="63%">
Creates an alternate location mapping for the specified file or files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50cb0b16-9ed3-4496-962a-9c845c10986c">AddComponent</a>
</td>
<td align="left" width="63%">
Adds a component to the list of components to be backed up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a4e2638-f6e7-4264-997d-41880f23c981">AddNewTarget</a>
</td>
<td align="left" width="63%">
Adds a new target location to which a file is to be restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8eea27d7-6780-49cf-97ea-8876a9a2c8f8">AddRestoreSubcomponent</a>
</td>
<td align="left" width="63%">
Adds a subcomponent to be restored and allows a requester to restore a portion of the entire
     component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c20e386-7cd8-45d9-92d6-96d0a458db50">AddToSnapshotSet</a>
</td>
<td align="left" width="63%">
Adds shadow copies to the shadow copy set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">BackupComplete</a>
</td>
<td align="left" width="63%">
Signals writers that the backup process has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c366f19-b10f-46cd-b5dc-cc3c77c5a008">BreakSnapshotSet</a>
</td>
<td align="left" width="63%">
Causes the existence of a shadow copy set to be "forgotten" by VSS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e06f69e-8210-4773-8080-5c58e6f59792">DeleteSnapshots</a>
</td>
<td align="left" width="63%">
Deletes one or more shadow copies or a shadow copy set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7567bf23-4f4c-4210-87f7-4f90262fda7a">DisableWriterClasses</a>
</td>
<td align="left" width="63%">
Disables the requesting of writer metadata from the specified writer classes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/746fb12d-83d7-463d-848d-36e095832d1a">DisableWriterInstances</a>
</td>
<td align="left" width="63%">
Disables the specified writer instances.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cc6c375-8a24-4af3-b4ad-5a695cc2645c">DoSnapshotSet</a>
</td>
<td align="left" width="63%">
Commits all shadow copies in this set simultaneously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27dae374-f3c4-44a5-a0d7-3edb647f0593">EnableWriterClasses</a>
</td>
<td align="left" width="63%">
Enables the requesting of writer metadata from the specified writer classes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a0abafa-d770-4529-90e4-0c597729d525">ExposeSnapshot</a>
</td>
<td align="left" width="63%">
Exposes the specified shadow copy as a drive letter, mounted folder, or file
     share.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/888d30bd-527b-4b7b-9d31-3df0556b268f">FreeWriterMetadata</a>
</td>
<td align="left" width="63%">
Frees system resources allocated when 
    <a href="https://msdn.microsoft.com/44f19c10-c966-4ab6-98dd-865d535955db">GatherWriterMetadata</a> is 
     called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2bf4c575-f94d-43df-b141-94ed5a55294b">FreeWriterStatus</a>
</td>
<td align="left" width="63%">
Frees system resources allocated during the call to 
     <a href="https://msdn.microsoft.com/ca87cdc3-e233-4efc-81c0-918e5a698af5">GatherWriterStatus</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44f19c10-c966-4ab6-98dd-865d535955db">GatherWriterMetadata</a>
</td>
<td align="left" width="63%">
Prompts each writer to send the metadata it has collected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca87cdc3-e233-4efc-81c0-918e5a698af5">GatherWriterStatus</a>
</td>
<td align="left" width="63%">
Prompts each writer to send a status message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4e2f9f3-7dee-4324-a48a-6de2a32eabf7">GetSnapshotProperties</a>
</td>
<td align="left" width="63%">
Gets the properties of the specified shadow copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b99e7e41-1c88-462c-b6d8-734f7a6e24d4">GetWriterComponents</a>
</td>
<td align="left" width="63%">
Obtains a specific writer component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39ab6179-2828-46dc-bfcd-0dd62c34ce95">GetWriterComponentsCount</a>
</td>
<td align="left" width="63%">
Gets the number of writer components.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a577d06a-4c9d-4ebe-b4d4-685f96ec9c83">GetWriterMetadata</a>
</td>
<td align="left" width="63%">
Returns writer metadata for a specific writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf8c4782-2850-4847-a7a1-95bd2bd547a1">GetWriterMetadataCount</a>
</td>
<td align="left" width="63%">
Returns the number of writers for which there is metadata.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/652e9630-291d-41cd-96d9-6a63988932a5">GetWriterStatus</a>
</td>
<td align="left" width="63%">
Returns the status of the specified writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e358cb2b-9b0f-47fb-a0ca-7bbbc6e49aff">GetWriterStatusCount</a>
</td>
<td align="left" width="63%">
Returns the number of writers for which there is status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f28c841-5448-4ed7-b76e-0aa5376fd8bf">ImportSnapshots</a>
</td>
<td align="left" width="63%">
Imports shadow copies transported from a different machine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df469964-c954-4f79-b88f-a521157a0c66">InitializeForBackup</a>
</td>
<td align="left" width="63%">
Initializes the backup components metadata file in preparation for backup.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8ba1463-4da7-4539-8ade-b57ecda0a645">InitializeForRestore</a>
</td>
<td align="left" width="63%">
Initializes the <b>IVssBackupComponents</b> interface 
     in preparation for a restore operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42e069cb-3d9a-4592-bbb8-0113f14ed28c">IsVolumeSupported</a>
</td>
<td align="left" width="63%">
Determines whether the specified provider supports shadow copies for the specified volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01cf3931-59ef-4572-9f2e-aa210da0ac2d">PostRestore</a>
</td>
<td align="left" width="63%">
Signals the <a href="https://msdn.microsoft.com/01cf3931-59ef-4572-9f2e-aa210da0ac2d">PostRestore</a> event to 
     the writers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46ce8282-a434-4b0b-b66e-40810052b34b">PrepareForBackup</a>
</td>
<td align="left" width="63%">
Signals all writers that a backup is about to occur.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">PreRestore</a>
</td>
<td align="left" width="63%">
Signals the <a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">PreRestore</a> event to 
     the writers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f79bf84-c7b9-4291-ae3b-7061fe3199e9">Query</a>
</td>
<td align="left" width="63%">
Queries the list of providers or shadow copies in the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2e97723-98cb-401c-ab35-20c004f0a73d">QueryRevertStatus</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/d2cff547-b4ff-454d-8e0e-cd29b91cbb07">IVssAsync</a> interface pointer that can be used 
   to determine the status of the revert operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9976195e-3448-4b0e-82b2-1ae061c75b17">RevertToSnapshot</a>
</td>
<td align="left" width="63%">
Reverts a volume to a previous shadow copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8184d15a-7d1f-49ed-afe3-fa9d81a4d32d">SaveAsXML</a>
</td>
<td align="left" width="63%">
Saves the specified backup component metadata file to the storage media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3a38348-ab89-40a5-bf77-612bcd99c31b">SetAdditionalRestores</a>
</td>
<td align="left" width="63%">
Indicates whether additional restores of the component will follow this restore (that is, full restore
     followed by log file restores).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b9a64b2-2bc9-441b-97f7-a72fd7579126">SetBackupOptions</a>
</td>
<td align="left" width="63%">
Sets a string of private, or writer-dependent, backup parameters for a writer component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18a1295d-b763-477b-bda2-baf8a878bf46">SetBackupState</a>
</td>
<td align="left" width="63%">
Defines an overall configuration for a backup operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5565183d-f374-4796-a399-b008041afdd2">SetBackupSucceeded</a>
</td>
<td align="left" width="63%">
Indicates whether the backup of the specified component was successful.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e466090-b551-44e8-a86d-75126352aa49">SetContext</a>
</td>
<td align="left" width="63%">
Sets the context for all subsequent shadow copy-related operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/669d61cc-c586-4dcc-a936-5343a393d371">SetFileRestoreStatus</a>
</td>
<td align="left" width="63%">
Requester indicates whether all, some, or none of the files were successfully restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc1c75bf-b281-4741-9273-f7264532860f">SetPreviousBackupStamp</a>
</td>
<td align="left" width="63%">
Sets a backup stamp indicating the time of a previous backup against which a differential or incremental
     backup is to be evaluated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/170f9ea0-4846-49d4-ab06-eb1ce580e827">SetRangesFilePath</a>
</td>
<td align="left" width="63%">
Indicates that the ranges file used in a partial file operation has been restored to a new location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a872594-dcd8-463d-9f6b-6bc40c17df38">SetRestoreOptions</a>
</td>
<td align="left" width="63%">
Sets a string of private, or writer-dependent, restore parameters for a writer component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc85e93f-1034-41cc-bf69-025aa86a56fd">SetRestoreState</a>
</td>
<td align="left" width="63%">
Sets how a restore will be processed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f8051d3-b1b6-418b-8a53-0ddc82a20bb3">SetSelectedForRestore</a>
</td>
<td align="left" width="63%">
Indicates whether the specified component has been selected for restoration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a0a6228-2131-48a6-8d18-9491969d265b">StartSnapshotSet</a>
</td>
<td align="left" width="63%">
Creates a new, empty shadow copy set.

</td>
</tr>
</table> 

