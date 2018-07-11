---
UID: NL:vswriter.IVssComponent
title: IVssComponent
author: windows-sdk-content
description: The IVssComponent interface is a C++ (not COM) interface containing methods for examining and modifying information about components contained in a requester's Backup Components Document.
old-location: base\ivsscomponent.htm
old-project: vss
ms.assetid: c686a424-b0b9-4efc-8dc6-b92193de2a5d
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IVssComponent, IVssComponent interface [VSS], IVssComponent interface [VSS],described, _win32_ivsscomponent, base.ivsscomponent, vswriter/IVssComponent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
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
 - IVssComponent
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssComponent class


## -description


The <b>IVssComponent</b> interface is a C++ (not COM) interface 
    containing methods for examining and modifying information about components contained in a requester's Backup 
    Components Document.

<b>IVssComponent</b> objects can be obtained only for those 
    components that have been explicitly added to the Backup Components Document during a backup operation by the 
    <a href="https://msdn.microsoft.com/50cb0b16-9ed3-4496-962a-9c845c10986c">IVssBackupComponents::AddComponent</a> 
    method.

Information about components explicitly added during a restore operation using 
    <a href="https://msdn.microsoft.com/8eea27d7-6780-49cf-97ea-8876a9a2c8f8"> IVssBackupComponents::AddRestoreSubcomponent</a> 
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
    <a href="https://msdn.microsoft.com/e8920cca-d944-437f-bf6a-7ce8d518746a">Working with Selectability and 
    Logical Paths</a>).

The interface can be used by either a writer or a requester, although certain methods are supported only for 
    writers. In this way, a writer can request changes in a backup or restore operation, such as adding a new target, 
    or learn of requester actions, such as the use of an alternate location.

The following methods return an <b>IVssComponent</b> 
    interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/ee816d83-31f3-47ff-b581-cc4dcd878f22">IVssWriterComponents::GetComponent</a>
</li>
<li>
<a href="https://msdn.microsoft.com/29772c1f-1cc4-4ee7-8e1d-f1a6cbebf470">IVssWriterComponentsExt::GetComponent</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssComponent</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVssComponent</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e708a6e9-9e4e-4620-8251-65b14a7bc6ee">AddDifferencedFilesByLastModifyLSN</a>
</td>
<td align="left" width="63%">
Reserved for system use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33372d10-c947-45de-9ea2-03ba6378179d">AddDifferencedFilesByLastModifyTime</a>
</td>
<td align="left" width="63%">
Used by supporting writers to return its differenced files for incremental or differential backup on the 
     basis of the time of the last file modification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/927865ff-f3c4-4863-913e-cfffb7bbdbb2">AddDirectedTarget</a>
</td>
<td align="left" width="63%">
Adds a directed target specification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/318dc1ee-e63f-4e79-96b9-8a8bd83facd3">AddPartialFile</a>
</td>
<td align="left" width="63%">
Indicates that only portions of a file are to be backed up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f398a88a-6572-4d0b-a241-37cc0e9e99a0">GetAdditionalRestores</a>
</td>
<td align="left" width="63%">
Indicates whether additional restores will occur for the current component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c6537eb-67ba-4d6a-ac86-44da176ef5c5">GetAlternateLocationMapping</a>
</td>
<td align="left" width="63%">
Returns the location of data restored to an alternate location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/218dc021-0a9e-4ba7-95b7-e1f31e57e71c">GetAlternateLocationMappingCount</a>
</td>
<td align="left" width="63%">
Returns the number of alternate location mappings used by a requester in restoring data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/638b8909-0aef-4066-ade7-4ee6d96b309e">GetBackupMetadata</a>
</td>
<td align="left" width="63%">
Returns the backup metadata set by 
     <a href="https://msdn.microsoft.com/4e88d92b-48f3-42f9-bf66-61337a745902">CVssWriter::OnPrepareBackup</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54182058-5dbb-4eda-959a-fa1921a27302">GetBackupOptions</a>
</td>
<td align="left" width="63%">
Returns the backup options associated with the writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8f272d8-4024-46bf-a0e6-77d870615fc0">GetBackupStamp</a>
</td>
<td align="left" width="63%">
Returns a store backup stamp.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b2dce08-a4ab-4e55-aeef-819f71ddf9d2">GetBackupSucceeded</a>
</td>
<td align="left" width="63%">
Indicates whether the backup operation was successful.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24b36ea6-3662-4846-a90b-5c2da578e1fa">GetComponentName</a>
</td>
<td align="left" width="63%">
Returns the logical name of this component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89675df6-dcfd-4167-aa6f-5c88e619ef1c">GetComponentType</a>
</td>
<td align="left" width="63%">
Returns the type of this component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/285b2ac7-d09e-4ac5-bf5c-62c510544353">GetDifferencedFile</a>
</td>
<td align="left" width="63%">
Returns information about a specified file specification supporting an incremental or differential backup or 
     restore as a differenced file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46faeb2b-7d83-4618-ba36-bdacc5ca055d">GetDifferencedFilesCount</a>
</td>
<td align="left" width="63%">
Returns the number of file specifications marked by a writer as supporting an incremental or differential 
     backup or restore as a differenced file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e25760b0-14e2-4f1b-b4ff-e7b78f0b7b12">GetDirectedTarget</a>
</td>
<td align="left" width="63%">
Returns information about a specified directed target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c8cf80e-66b9-4c6f-a63d-90626937582b">GetDirectedTargetCount</a>
</td>
<td align="left" width="63%">
Returns the number of directed target specifications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b79c4443-c850-4edf-bdd2-917e22e67d77">GetFileRestoreStatus</a>
</td>
<td align="left" width="63%">
Determines whether all of the files were successfully restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16c85322-5127-40aa-8393-df7684cd1c92">GetLogicalPath</a>
</td>
<td align="left" width="63%">
Returns the logical path of this component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21f22fae-2230-418b-8942-754c863a9213">GetNewTarget</a>
</td>
<td align="left" width="63%">
Returns information about a new target restore location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b41afed9-2689-469e-b3c4-83cf18c5f8a9">GetNewTargetCount</a>
</td>
<td align="left" width="63%">
Returns the count of new target restore locations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed589ae8-2abb-4c3b-9695-12649fc89818">GetPartialFile</a>
</td>
<td align="left" width="63%">
Returns information on a partial file to be backed up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7be84c00-49c4-4c44-9c12-7994247726a5">GetPartialFileCount</a>
</td>
<td align="left" width="63%">
Returns the number of partial files to be backed up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7d236e9-bd83-4685-b249-4e5b8ada535a">GetPostRestoreFailureMsg</a>
</td>
<td align="left" width="63%">
Returns the failure message returned by the component's writer while handling the 
     <a href="https://msdn.microsoft.com/01cf3931-59ef-4572-9f2e-aa210da0ac2d">PostRestore</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58c007a8-8414-4e2d-8042-d249a723780a">GetPreRestoreFailureMsg</a>
</td>
<td align="left" width="63%">
Returns the failure message returned by the component's writer while handling the 
     <a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">PreRestore</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91778854-52af-4e1e-943b-89c786963291">GetPreviousBackupStamp</a>
</td>
<td align="left" width="63%">
Returns the backup stamp of an earlier backup operation upon which to base a differential or incremental 
     backup.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b53c523-a105-4507-89f3-1f746aa86204">GetRestoreMetadata</a>
</td>
<td align="left" width="63%">
Returns the restore metadata associated with the current component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/818fd713-1b41-4abd-aca4-c74383fa3594">GetRestoreOptions</a>
</td>
<td align="left" width="63%">
Returns the restore options associated with the writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23c37342-fcbd-4401-83d5-a52d4a69b908">GetRestoreSubcomponent</a>
</td>
<td align="left" width="63%">
Returns the specified subcomponent to be restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04c1dcdc-7672-4b7c-a9db-eafca80ab257">GetRestoreSubcomponentCount</a>
</td>
<td align="left" width="63%">
Returns the number of subcomponents to be restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2361e38-8757-4a29-bbaf-7f659d1095d9">GetRestoreTarget</a>
</td>
<td align="left" width="63%">
Returns the restore target associated with the current component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76d0461d-a0ac-49c7-84b1-16f21114b72d">IsSelectedForRestore</a>
</td>
<td align="left" width="63%">
Determines if the component has been selected to be restored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96d0a581-87a5-4f97-b23f-08e90a805de1">SetBackupMetadata</a>
</td>
<td align="left" width="63%">
Associates backup metadata with the component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54995cc9-8988-4f26-9c60-5d809a93e4e1">SetBackupStamp</a>
</td>
<td align="left" width="63%">
Sets the backup stamp indicating the time of a backup operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1059a586-69e2-4a02-8f52-b8da3f04f51c">SetPostRestoreFailureMsg</a>
</td>
<td align="left" width="63%">
Sets the failure message for the 
     <a href="https://msdn.microsoft.com/01cf3931-59ef-4572-9f2e-aa210da0ac2d">PostRestore</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b273cba-9878-4494-81ef-af1367f1e0a5">SetPreRestoreFailureMsg</a>
</td>
<td align="left" width="63%">
Sets the failure message for the 
     <a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">PreRestore</a> event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b329fa8-21ad-4de9-9857-52e14d51d429">SetRestoreMetadata</a>
</td>
<td align="left" width="63%">
Sets the restore metadata for the current component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e8b9322-6611-4a47-aa7a-876be01d33b8">SetRestoreTarget</a>
</td>
<td align="left" width="63%">
Sets the restore target for the current component.

</td>
</tr>
</table> 

