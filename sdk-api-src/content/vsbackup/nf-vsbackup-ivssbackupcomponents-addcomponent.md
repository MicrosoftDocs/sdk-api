---
UID: NF:vsbackup.IVssBackupComponents.AddComponent
title: IVssBackupComponents::AddComponent method
author: windows-driver-content
description: Used to explicitly add to the backup set.
old-location: base\ivssbackupcomponents_addcomponent.htm
old-project: VSS
ms.assetid: 50cb0b16-9ed3-4496-962a-9c845c10986c
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: AddComponent method [VSS], AddComponent method [VSS], IVssBackupComponents interface, AddComponent,IVssBackupComponents.AddComponent, IVssBackupComponents, IVssBackupComponents interface [VSS], AddComponent method, IVssBackupComponents::AddComponent, _win32_ivssbackupcomponents_addcomponent, base.ivssbackupcomponents_addcomponent, vsbackup/IVssBackupComponents::AddComponent
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
-	IVssBackupComponents.AddComponent
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssBackupComponents::AddComponent method


## -description


The <b>AddComponent</b> method is 
    used to explicitly add to the backup set in the Backup Components Document all required 
    components (nonselectable for backup components without a selectable for backup ancestor), and such optional 
    (selectable for backup) components as the requester considers necessary. Members of component sets (components 
    with a selectable for backup ancestor) are implicitly included in the backup set, but are not explicitly added to 
    the Backup Components Document.


## -parameters




### -param instanceId [in]

Identifies a specific instance of a writer.


### -param writerId [in]

Writer class identifier.


### -param ct




### -param wszLogicalPath [in]

<b>Null</b>-terminated wide character string containing the logical path of the selectable for backup component.
      For more information, see <a href="https://msdn.microsoft.com/663c8ca9-8f5b-48bd-af2d-b2d90de9e492">Logical Pathing of Components</a>.

A logical path is not required when adding a component. Therefore, the value of this parameter can be 
       <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-<b>NULL</b> logical path.


### -param wszComponentName [in]

<b>Null</b>-terminated wide character string containing the name of the selectable for backup component.
      

The value of this parameter cannot be <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-<b>NULL</b> logical path.


#### - componentType [in]

Identifies the type of the component. Refer to the documentation for 
      <a href="https://msdn.microsoft.com/ba3b726c-448a-46c0-8fa5-5793497aa385">VSS_COMPONENT_TYPE</a> for permitted input values.


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
Successfully added the component.

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
The backup components object is not initialized, this method has been called during a restore operation, 
        or this method has not been called within the correct sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more 
        information, see 
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The object is a duplicate. A component with the same logical path and component name already 
        exists.

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



The <b>AddComponent</b> method has meaning only if 
    the backup operation takes place in component mode.

Only <a href="vssgloss_s.htm">selectable for backup 
    components</a> and nonselectable for backup components with no selectable for backup ancestors should be added 
    to the Backup Components Document using 
    <b>AddComponent</b>.

Nonselectable for backup components that have a selectable for backup ancestor in the hierarchy of their 
    logical paths are part of a component set defined by the selectable for backup ancestor. These components are 
    implicitly added to the Backup Components Document when the ancestor is added and should never be explicitly added 
    to a requester's Backup Components Document by using 
    <b>AddComponent</b>.The result of doing so is 
    undefined (see <a href="https://msdn.microsoft.com/e8920cca-d944-437f-bf6a-7ce8d518746a">Working with 
    Selectability and Logical Paths</a>).

Selectable for backup components with selectable for backup ancestors are also subcomponents in a component 
    set. They can be implicitly selected if their ancestor is selected (in which case they are not added to the Backup 
    Components Document using 
    <b>AddComponent</b>), or they can be 
    explicitly selected using 
    <b>AddComponent</b>.

The combination of logical path and name for each component of a given instance of a given class of writer 
    must be unique. Attempting to call 
    <b>AddComponent</b> twice with the same values 
    of <i>wszLogicalPath</i> and <i>wszComponentName</i> results in a 
    VSS_E_OBJECT_ALREADY_EXISTS error.

The distinction between the <i>instanceId</i> and the <i>writerID</i> is 
    necessary because it is possible to run multiple copies for the same writer.

A writer's class identifier and instance can be found by calling 
    <a href="https://msdn.microsoft.com/55240ef2-f480-4917-98f9-e88a2e23edea">IVssExamineWriterMetadata::GetIdentity</a>.

Before it calls <b>AddComponent</b>, a 
    requester must have been initialized for backup by calling 
    <a href="https://msdn.microsoft.com/df469964-c954-4f79-b88f-a521157a0c66">IVssBackupComponents::InitializeForBackup</a> and <a href="https://msdn.microsoft.com/44f19c10-c966-4ab6-98dd-865d535955db">IVssBackupComponents::GatherWriterMetadata</a>. See <a href="https://msdn.microsoft.com/1fc46062-c4a0-4aa2-ae05-3d7cded18584">Overview of Backup Initialization</a>.

The requester must call <b>AddComponent</b> to add the required components to the shadow copy before calling <a href="https://msdn.microsoft.com/3cc6c375-8a24-4af3-b4ad-5a695cc2645c">IVssBackupComponents::DoSnapshotSet</a> to create the shadow copy. See <a href="https://msdn.microsoft.com/04658d50-04f0-4189-8b88-ff152f1bf482">Overview of the Backup Discovery Phase</a> and <a href="https://msdn.microsoft.com/e6b082af-719b-4426-8217-0fc940f5884d">Overview of Pre-Backup Tasks</a>.




## -see-also




<a href="https://msdn.microsoft.com/a427ebbd-b7c4-46ba-ba16-dd601b1f956e">CVssWriter::Initialize</a>



<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/46ce8282-a434-4b0b-b66e-40810052b34b">IVssBackupComponents::PrepareForBackup</a>



<a href="https://msdn.microsoft.com/55240ef2-f480-4917-98f9-e88a2e23edea">IVssExamineWriterMetadata::GetIdentity</a>



<a href="https://msdn.microsoft.com/ba3b726c-448a-46c0-8fa5-5793497aa385">VSS_COMPONENT_TYPE</a>
 

 

