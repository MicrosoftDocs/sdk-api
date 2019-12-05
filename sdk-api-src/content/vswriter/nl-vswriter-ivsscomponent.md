---
UID: NL:vswriter.IVssComponent
title: IVssComponent (vswriter.h)
description: The IVssComponent interface is a C++ (not COM) interface containing methods for examining and modifying information about components contained in a requester's Backup Components Document.
old-location: base\ivsscomponent.htm
tech.root: VSS
ms.assetid: c686a424-b0b9-4efc-8dc6-b92193de2a5d
ms.date: 12/05/2018
ms.keywords: IVssComponent, IVssComponent interface [VSS], IVssComponent interface [VSS],described, _win32_ivsscomponent, base.ivsscomponent, vswriter/IVssComponent
ms.topic: class
f1_keywords:
- vswriter/IVssComponent
dev_langs:
- c++
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
- IVssComponent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssComponent class


## -description


The <b>IVssComponent</b> interface is a C++ (not COM) interface 
    containing methods for examining and modifying information about components contained in a requester's Backup 
    Components Document.

<b>IVssComponent</b> objects can be obtained only for those 
    components that have been explicitly added to the Backup Components Document during a backup operation by the 
    <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a> 
    method.

Information about components explicitly added during a restore operation using 
    <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent"> IVssBackupComponents::AddRestoreSubcomponent</a> 
    are not available through the <b>IVssComponent</b> interface.

Some information common to both components and implicitly selected subcomponents available through 
    <b>IVssComponent</b> objects includes the following:
<ul>
<li>Backup time stamp</li>
<li>Pre-/post-restore Failure Messages</li>
<li>Restore metadata</li>
<li>Restore target</li>
</ul>Some information in the <b>IVssComponent</b> object is on a 
    per-file basis and can refer to files managed either by explicitly selected components or by implicitly selected 
    subcomponents:
<ul>
<li>Alternate location mappings</li>
<li>Partial files</li>
<li>Directed target</li>
</ul>Other information is not included in the Backup Components Document and can be inferred using the 
    <b>IVssComponent</b> object in conjunction with the appropriate 
    Writer Metadata Documents based on a writer's component hierarchy expressed in the logical paths (see 
    <a href="https://docs.microsoft.com/windows/desktop/VSS/working-with-selectability-and-logical-paths">Working with Selectability and 
    Logical Paths</a>).

The interface can be used by either a writer or a requester, although certain methods are supported only for 
    writers. In this way, a writer can request changes in a backup or restore operation, such as adding a new target, 
    or learn of requester actions, such as the use of an alternate location.

The following methods return an <b>IVssComponent</b> 
    interface:
<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsswritercomponents-getcomponent">IVssWriterComponents::GetComponent</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivsswritercomponentsext">IVssWriterComponentsExt::GetComponent</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssComponent</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssComponent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssComponent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifylsn">AddDifferencedFilesByLastModifyLSN</a>
</td>
<td align="left" width="63%">
Reserved for system use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime">AddDifferencedFilesByLastModifyTime</a>
</td>
<td align="left" width="63%">
Used by supporting writers to return its differenced files for incremental or differential backup on the 
     basis of the time of the last file modification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-adddirectedtarget">AddDirectedTarget</a>
</td>
<td align="left" width="63%">
Adds a directed target specification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-addpartialfile">AddPartialFile</a>
</td>
<td align="left" width="63%">
Indicates that only portions of a file are to be backed up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getadditionalrestores">GetAdditionalRestores</a>
</td>
<td align="left" width="63%">
Indicates whether additional restores will occur for the current component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getalternatelocationmapping">GetAlternateLocationMapping</a>
</td>
<td align="left" width="63%">
Returns the location of data restored to an alternate location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount">GetAlternateLocationMappingCount</a>
</td>
<td align="left" width="63%">
Returns the number of alternate location mappings used by a requester in restoring data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getbackupmetadata">GetBackupMetadata</a>
</td>
<td align="left" width="63%">
Returns the backup metadata set by 
     <a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">CVssWriter::OnPrepareBackup</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getbackupoptions">GetBackupOptions</a>
</td>
<td align="left" width="63%">
Returns the backup options associated with the writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getbackupstamp">GetBackupStamp</a>
</td>
<td align="left" width="63%">
Returns a store backup stamp.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getbackupsucceeded">GetBackupSucceeded</a>
</td>
<td align="left" width="63%">
Indicates whether the backup operation was successful.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getcomponentname">GetComponentName</a>
</td>
<td align="left" width="63%">
Returns the logical name of this component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getcomponenttype">GetComponentType</a>
</td>
<td align="left" width="63%">
Returns the type of this component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getdifferencedfile">GetDifferencedFile</a>
</td>
<td align="left" width="63%">
Returns information about a specified file specification supporting an incremental or differential backup or 
     restore as a differenced file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getdifferencedfilescount">GetDifferencedFilesCount</a>
</td>
<td align="left" width="63%">
Returns the number of file specifications marked by a writer as supporting an incremental or differential 
     backup or restore as a differenced file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getdirectedtarget">GetDirectedTarget</a>
</td>
<td align="left" width="63%">
Returns information about a specified directed target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getdirectedtargetcount">GetDirectedTargetCount</a>
</td>
<td align="left" width="63%">
Returns the number of directed target specifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getfilerestorestatus">GetFileRestoreStatus</a>
</td>
<td align="left" width="63%">
Determines whether all of the files were successfully restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getlogicalpath">GetLogicalPath</a>
</td>
<td align="left" width="63%">
Returns the logical path of this component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getnewtarget">GetNewTarget</a>
</td>
<td align="left" width="63%">
Returns information about a new target restore location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getnewtargetcount">GetNewTargetCount</a>
</td>
<td align="left" width="63%">
Returns the count of new target restore locations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getpartialfile">GetPartialFile</a>
</td>
<td align="left" width="63%">
Returns information on a partial file to be backed up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getpartialfilecount">GetPartialFileCount</a>
</td>
<td align="left" width="63%">
Returns the number of partial files to be backed up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getpostrestorefailuremsg">GetPostRestoreFailureMsg</a>
</td>
<td align="left" width="63%">
Returns the failure message returned by the component's writer while handling the 
     <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-postrestore">PostRestore</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getprerestorefailuremsg">GetPreRestoreFailureMsg</a>
</td>
<td align="left" width="63%">
Returns the failure message returned by the component's writer while handling the 
     <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">PreRestore</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp">GetPreviousBackupStamp</a>
</td>
<td align="left" width="63%">
Returns the backup stamp of an earlier backup operation upon which to base a differential or incremental 
     backup.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getrestoremetadata">GetRestoreMetadata</a>
</td>
<td align="left" width="63%">
Returns the restore metadata associated with the current component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getrestoreoptions">GetRestoreOptions</a>
</td>
<td align="left" width="63%">
Returns the restore options associated with the writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getrestoresubcomponent">GetRestoreSubcomponent</a>
</td>
<td align="left" width="63%">
Returns the specified subcomponent to be restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getrestoresubcomponentcount">GetRestoreSubcomponentCount</a>
</td>
<td align="left" width="63%">
Returns the number of subcomponents to be restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getrestoretarget">GetRestoreTarget</a>
</td>
<td align="left" width="63%">
Returns the restore target associated with the current component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-isselectedforrestore">IsSelectedForRestore</a>
</td>
<td align="left" width="63%">
Determines if the component has been selected to be restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-setbackupmetadata">SetBackupMetadata</a>
</td>
<td align="left" width="63%">
Associates backup metadata with the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-setbackupstamp">SetBackupStamp</a>
</td>
<td align="left" width="63%">
Sets the backup stamp indicating the time of a backup operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg">SetPostRestoreFailureMsg</a>
</td>
<td align="left" width="63%">
Sets the failure message for the 
     <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-postrestore">PostRestore</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg">SetPreRestoreFailureMsg</a>
</td>
<td align="left" width="63%">
Sets the failure message for the 
     <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-prerestore">PreRestore</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-setrestoremetadata">SetRestoreMetadata</a>
</td>
<td align="left" width="63%">
Sets the restore metadata for the current component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-setrestoretarget">SetRestoreTarget</a>
</td>
<td align="left" width="63%">
Sets the restore target for the current component.

</td>
</tr>
</table> 

