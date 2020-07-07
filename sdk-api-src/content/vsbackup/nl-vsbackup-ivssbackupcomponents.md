---
UID: NL:vsbackup.IVssBackupComponents
title: IVssBackupComponents (vsbackup.h)
description: The IVssBackupComponents interface is used by a requester to poll writers about file status and to run backup/restore operations.
helpviewer_keywords: ["IVssBackupComponents","IVssBackupComponents interface [VSS]","IVssBackupComponents interface [VSS]","described","_win32_ivssbackupcomponents","base.ivssbackupcomponents","vsbackup/IVssBackupComponents"]
old-location: base\ivssbackupcomponents.htm
tech.root: VSS
ms.assetid: fe1220c7-11e5-4872-b7a9-61558f7c75c0
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents, IVssBackupComponents interface [VSS], IVssBackupComponents interface [VSS],described, _win32_ivssbackupcomponents, base.ivssbackupcomponents, vsbackup/IVssBackupComponents
f1_keywords:
- vsbackup/IVssBackupComponents
dev_langs:
- c++
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
    <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-createvssbackupcomponents">CreateVssBackupComponents</a>.

An <b>IVssBackupComponents</b> object can be used for 
    only a single backup, restore, or <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-query">Query</a> operation.

After the backup, restore, or <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-query">Query</a> operation has either successfully finished or been explicitly terminated, a requester must 
    release the <b>IVssBackupComponents</b> object by calling 
    <b>IVssBackupComponents::Release</b>. An 
    <b>IVssBackupComponents</b> object must not be reused. For example, you cannot perform a backup or restore operation with the same <b>IVssBackupComponents</b> object that you have already used for a <b>Query</b> operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssBackupComponents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssBackupComponents</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-abortbackup">AbortBackup</a>
</td>
<td align="left" width="63%">
Terminates the current backup.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping">AddAlternativeLocationMapping</a>
</td>
<td align="left" width="63%">
Creates an alternate location mapping for the specified file or files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">AddComponent</a>
</td>
<td align="left" width="63%">
Adds a component to the list of components to be backed up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addnewtarget">AddNewTarget</a>
</td>
<td align="left" width="63%">
Adds a new target location to which a file is to be restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent">AddRestoreSubcomponent</a>
</td>
<td align="left" width="63%">
Adds a subcomponent to be restored and allows a requester to restore a portion of the entire
     component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset">AddToSnapshotSet</a>
</td>
<td align="left" width="63%">
Adds shadow copies to the shadow copy set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-backupcomplete">BackupComplete</a>
</td>
<td align="left" width="63%">
Signals writers that the backup process has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset">BreakSnapshotSet</a>
</td>
<td align="left" width="63%">
Causes the existence of a shadow copy set to be "forgotten" by VSS.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots">DeleteSnapshots</a>
</td>
<td align="left" width="63%">
Deletes one or more shadow copies or a shadow copy set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-disablewriterclasses">DisableWriterClasses</a>
</td>
<td align="left" width="63%">
Disables the requesting of writer metadata from the specified writer classes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-disablewriterinstances">DisableWriterInstances</a>
</td>
<td align="left" width="63%">
Disables the specified writer instances.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset">DoSnapshotSet</a>
</td>
<td align="left" width="63%">
Commits all shadow copies in this set simultaneously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-enablewriterclasses">EnableWriterClasses</a>
</td>
<td align="left" width="63%">
Enables the requesting of writer metadata from the specified writer classes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot">ExposeSnapshot</a>
</td>
<td align="left" width="63%">
Exposes the specified shadow copy as a drive letter, mounted folder, or file
     share.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-freewritermetadata">FreeWriterMetadata</a>
</td>
<td align="left" width="63%">
Frees system resources allocated when 
    <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata">GatherWriterMetadata</a> is 
     called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-freewriterstatus">FreeWriterStatus</a>
</td>
<td align="left" width="63%">
Frees system resources allocated during the call to 
     <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus">GatherWriterStatus</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata">GatherWriterMetadata</a>
</td>
<td align="left" width="63%">
Prompts each writer to send the metadata it has collected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus">GatherWriterStatus</a>
</td>
<td align="left" width="63%">
Prompts each writer to send a status message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties">GetSnapshotProperties</a>
</td>
<td align="left" width="63%">
Gets the properties of the specified shadow copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents">GetWriterComponents</a>
</td>
<td align="left" width="63%">
Obtains a specific writer component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount">GetWriterComponentsCount</a>
</td>
<td align="left" width="63%">
Gets the number of writer components.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata">GetWriterMetadata</a>
</td>
<td align="left" width="63%">
Returns writer metadata for a specific writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount">GetWriterMetadataCount</a>
</td>
<td align="left" width="63%">
Returns the number of writers for which there is metadata.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus">GetWriterStatus</a>
</td>
<td align="left" width="63%">
Returns the status of the specified writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount">GetWriterStatusCount</a>
</td>
<td align="left" width="63%">
Returns the number of writers for which there is status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-importsnapshots">ImportSnapshots</a>
</td>
<td align="left" width="63%">
Imports shadow copies transported from a different machine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup">InitializeForBackup</a>
</td>
<td align="left" width="63%">
Initializes the backup components metadata file in preparation for backup.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore">InitializeForRestore</a>
</td>
<td align="left" width="63%">
Initializes the <b>IVssBackupComponents</b> interface 
     in preparation for a restore operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-isvolumesupported">IsVolumeSupported</a>
</td>
<td align="left" width="63%">
Determines whether the specified provider supports shadow copies for the specified volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-postrestore">PostRestore</a>
</td>
<td align="left" width="63%">
Signals the <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-postrestore">PostRestore</a> event to 
     the writers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup">PrepareForBackup</a>
</td>
<td align="left" width="63%">
Signals all writers that a backup is about to occur.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">PreRestore</a>
</td>
<td align="left" width="63%">
Signals the <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">PreRestore</a> event to 
     the writers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-query">Query</a>
</td>
<td align="left" width="63%">
Queries the list of providers or shadow copies in the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-queryrevertstatus">QueryRevertStatus</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface pointer that can be used 
   to determine the status of the revert operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-reverttosnapshot">RevertToSnapshot</a>
</td>
<td align="left" width="63%">
Reverts a volume to a previous shadow copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-saveasxml">SaveAsXML</a>
</td>
<td align="left" width="63%">
Saves the specified backup component metadata file to the storage media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores">SetAdditionalRestores</a>
</td>
<td align="left" width="63%">
Indicates whether additional restores of the component will follow this restore (that is, full restore
     followed by log file restores).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions">SetBackupOptions</a>
</td>
<td align="left" width="63%">
Sets a string of private, or writer-dependent, backup parameters for a writer component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setbackupstate">SetBackupState</a>
</td>
<td align="left" width="63%">
Defines an overall configuration for a backup operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded">SetBackupSucceeded</a>
</td>
<td align="left" width="63%">
Indicates whether the backup of the specified component was successful.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setcontext">SetContext</a>
</td>
<td align="left" width="63%">
Sets the context for all subsequent shadow copy-related operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus">SetFileRestoreStatus</a>
</td>
<td align="left" width="63%">
Requester indicates whether all, some, or none of the files were successfully restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp">SetPreviousBackupStamp</a>
</td>
<td align="left" width="63%">
Sets a backup stamp indicating the time of a previous backup against which a differential or incremental
     backup is to be evaluated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath">SetRangesFilePath</a>
</td>
<td align="left" width="63%">
Indicates that the ranges file used in a partial file operation has been restored to a new location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions">SetRestoreOptions</a>
</td>
<td align="left" width="63%">
Sets a string of private, or writer-dependent, restore parameters for a writer component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setrestorestate">SetRestoreState</a>
</td>
<td align="left" width="63%">
Sets how a restore will be processed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore">SetSelectedForRestore</a>
</td>
<td align="left" width="63%">
Indicates whether the specified component has been selected for restoration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset">StartSnapshotSet</a>
</td>
<td align="left" width="63%">
Creates a new, empty shadow copy set.

</td>
</tr>
</table> 

