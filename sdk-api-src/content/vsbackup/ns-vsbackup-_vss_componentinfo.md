---
UID: NS:vsbackup._VSS_COMPONENTINFO
title: "_VSS_COMPONENTINFO"
author: windows-sdk-content
description: Contains information about a given component.
old-location: base\vss_componentinfo.htm
tech.root: VSS
ms.assetid: 9723e90e-cd5e-4815-843b-8ed8632ebe45
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PVSSCOMPONENTINFO, PVSSCOMPONENTINFO structure pointer [VSS], VSS_COMPONENTINFO, VSS_COMPONENTINFO structure [VSS], _VSS_COMPONENTINFO, _win32_vss_componentinfo, base.vss_componentinfo, vsbackup/PVSSCOMPONENTINFO, vsbackup/VSS_COMPONENTINFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VsBackup.h
api_name:
 - VSS_COMPONENTINFO
product: Windows
targetos: Windows
req.typenames: VSS_COMPONENTINFO
req.redist: 
---

# _VSS_COMPONENTINFO structure


## -description


The <b>VSS_COMPONENTINFO</b> structure contains 
    information about a given component, and is returned to requesters by the 
    <a href="https://msdn.microsoft.com/8567ca7f-dc50-4cf2-b3c1-a2ae8d55dc95">IVssWMComponent</a> interface.


## -struct-fields




### -field type

Component type. See <a href="https://msdn.microsoft.com/ba3b726c-448a-46c0-8fa5-5793497aa385">VSS_COMPONENT_TYPE</a>.


### -field bstrLogicalPath

A string containing the logical path of the component. 
      

A logical path can be <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-<b>NULL</b> logical path.


### -field bstrComponentName

A string containing the name of the component. A component name string cannot be <b>NULL</b>.


### -field bstrCaption

A string containing the description of the component. A caption string can be <b>NULL</b>.


### -field pbIcon

Pointer to a buffer containing the binary data for a displayable icon representing the component. The 
      buffer contents should use the same format as the standard icon (.ico) files. The size, in bytes, of the buffer 
      is specified by <b>cbIcon</b>.
      

If the writer that created the component did not choose to specify an icon, <b>pbIcon</b> 
       is <b>NULL</b>.


### -field cbIcon

The size, in bytes, of the displayable icon (<b>pbIcon</b>) representing the component. 
      If <b>pbIcon</b> is <b>NULL</b>, <b>cbIcon</b> should 
      be zero.


### -field bRestoreMetadata

Boolean that indicates whether there is private metadata associated with the restoration of the component. 
      The Boolean is <b>true</b> if there is metadata and <b>false</b> if there 
      is not.
      

A writer indicates whether a component supports private metadata by setting this value when a component is 
       added with 
       <a href="https://msdn.microsoft.com/fdbcbcea-d49e-49bc-9bb8-2210a9de02a4">IVssCreateWriterMetadata::AddComponent</a>. 
       Writers later add restore metadata with 
       <a href="https://msdn.microsoft.com/2b329fa8-21ad-4de9-9857-52e14d51d429">IVssComponent::SetRestoreMetadata</a>.
       Requesters retrieve the information using 
       <a href="https://msdn.microsoft.com/1b53c523-a105-4507-89f3-1f746aa86204">IVssComponent::GetRestoreMetadata</a>.


### -field bNotifyOnBackupComplete

Reserved for future use. The value of this parameter should always be set to 
      <b>false</b>.


### -field bSelectable

Boolean that indicates (for component mode operations) if the component is selectable for backup. The value 
      of <b>bSelectable</b> helps determine whether a requester has the option of including or 
      excluding a given component in backup operations. The Boolean is <b>true</b> if the component 
      is selectable for backup and <b>false</b> if it is not.
      

There is no default value for a component's selectability for backup. A writer must always explicitly set the 
       value when it adds the component to its Writer Metadata Document using 
       <a href="https://msdn.microsoft.com/fdbcbcea-d49e-49bc-9bb8-2210a9de02a4">IVssCreateWriterMetadata::AddComponent</a>.

In addition, the value of <b>bSelectable</b>, the component's logical path, and the 
       component's relationship to other components as expressed in that path determine when and how a component is 
       included in a backup operation:

<ul>
<li>For a nonselectable for backup component (<b>bSelectable</b> is 
        <b>false</b>) with no selectable for backup ancestors in the hierarchy of its logical path, 
        inclusion in the backup set is always mandatory and always implicit. 
        A requester explicitly adds the component to the backup set in the Backup Components Document with 
         <a href="https://msdn.microsoft.com/50cb0b16-9ed3-4496-962a-9c845c10986c">IVssBackupComponents::AddComponent</a>.

</li>
<li>For a selectable for backup component (<b>bSelectable</b> is 
        <b>true</b>) with no selectable for backup ancestor in the hierarchy of its logical paths, 
        inclusion in the backup set is always optional and always explicit. 
        A requester explicitly adds the component to the backup set in the Backup Components Document with 
         <a href="https://msdn.microsoft.com/50cb0b16-9ed3-4496-962a-9c845c10986c">IVssBackupComponents::AddComponent</a>.

If such a component is included as an ancestor in the logical path of other components, both those that are 
         selectable for backup and those that are not, it defines a component set containing these other components as 
         subcomponents. If a selectable for backup component is explicitly included in a backup, these subcomponents 
         are implicitly included in the backup.

</li>
<li>For a nonselectable for backup component (<b>bSelectable</b> is 
        <b>false</b>) that has a selectable for backup ancestor in the hierarchy of its logical 
        paths (and are therefore part of a component set defined by that ancestor), inclusion in the backup set is 
        always implicit and contingent on the inclusion of a selectable for backup ancestor. 
        A requester never explicitly adds the component to the backup set in the Backup Components Document; 
         instead, it adds the selectable for backup ancestor to the document using 
         <a href="https://msdn.microsoft.com/50cb0b16-9ed3-4496-962a-9c845c10986c">IVssBackupComponents::AddComponent</a>.

</li>
<li>For a selectable for backup component (<b>bSelectable</b> is 
        <b>true</b>) that has a selectable for backup ancestor in the hierarchy of its logical 
        paths (and is therefore part of a component set defined by that ancestor), inclusion in the backup set can be 
        either optional and explicit, or if the component is not explicitly selected, its inclusion may be implicit 
        and contingent on the inclusion of a selectable for backup ancestor. 
        If the inclusion of the component is explicit, a requester explicitly adds the components to the backup set 
         in the Backup Components Document with 
         <a href="https://msdn.microsoft.com/50cb0b16-9ed3-4496-962a-9c845c10986c">IVssBackupComponents::AddComponent</a>.

If the inclusion is implicit, a requester does not add these components to a backup set in the Backup 
         Components Document.

If the inclusion of the component is explicit and the component defines a component set, the members of 
         that component set are implicitly selected.

A writer sets a component's selectability for backup (<b>bSelectable</b>) when adding 
         the component to the Writer Metadata Document by using 
         <a href="https://msdn.microsoft.com/fdbcbcea-d49e-49bc-9bb8-2210a9de02a4">IVssCreateWriterMetadata::AddComponent</a>.

See <a href="https://msdn.microsoft.com/e8920cca-d944-437f-bf6a-7ce8d518746a">Working with Selectability 
         and Logical Paths</a> for more information.

</li>
</ul>

### -field bSelectableForRestore

Boolean that indicates (for component-mode operations) whether the component is selectable for restore. 
      <b>bSelectableForRestore</b> allows the requester to determine whether this component can be 
      individually selected for restore if it had earlier been 
      <a href="https://msdn.microsoft.com/en-us/library/Aa384659(v=VS.85).aspx">implicitly included</a> in the 
      backup. The Boolean is <b>true</b> if the component is selectable for restore and 
      <b>false</b> if it is not.
      

By default, a component's selectability for restore is <b>false</b>. A writer can override 
       this default when it adds the component to its Writer Metadata Document using 
       <a href="https://msdn.microsoft.com/fdbcbcea-d49e-49bc-9bb8-2210a9de02a4">IVssCreateWriterMetadata::AddComponent</a>.

If the component was <a href="vssgloss_e.htm">explicitly 
       added</a> to the backup document, it can always be individually selected for restore, so this flag then has 
       no meaning. If the component was implicitly added to the backup document, then the 
       <b>bSelectableForRestore</b> flag determines whether the component can be individually 
       restored using 
       <a href="https://msdn.microsoft.com/8eea27d7-6780-49cf-97ea-8876a9a2c8f8">IVssBackupComponents::AddRestoreSubcomponent</a>.

See <a href="https://msdn.microsoft.com/e8920cca-d944-437f-bf6a-7ce8d518746a">Working with Selectability 
       and Logical Paths</a> for more information.


### -field dwComponentFlags

A bit mask (or bitwise OR) of values of the 
      <a href="https://msdn.microsoft.com/91b7fbab-82f8-48cc-8078-f8f71c48a70b">VSS_COMPONENT_FLAGS</a> enumeration, indicating the 
      features this component supports.

<b>Windows Server 2003 and Windows XP:  </b>Before Windows Server 2003 with SP1, this member is reserved for system use.


### -field cFileCount

If the component is a file group, the number of file descriptors for files in the group. Otherwise, this 
      value is zero.


### -field cDatabases

If the component is a database, the number of database file descriptors. Otherwise, this value is 
      zero.


### -field cLogFiles

If the component is a database, the number of database log file descriptors. Otherwise, the value of this 
      parameter is zero.


### -field cDependencies

The number of explicit writer-component dependencies of the current component. This value is incremented 
      when 
      <a href="https://msdn.microsoft.com/cc6c8ab6-3706-4c75-ba31-cc8c1dc4dd06">IVssCreateWriterMetadata::AddComponentDependency</a> 
      is called by a writer.


## -remarks



To obtain  <b>VSS_COMPONENTINFO</b> object for a given 
    component, a requester must first obtain the corresponding 
    <a href="https://msdn.microsoft.com/8567ca7f-dc50-4cf2-b3c1-a2ae8d55dc95">IVssWMComponent</a> object through a call to 
    <a href="https://msdn.microsoft.com/fd03ac7c-8398-4972-85f1-2afe13317950">IVssExamineWriterMetadata::GetComponent</a>. 
    A call to 
    <a href="https://msdn.microsoft.com/ac01bfea-e60f-4f50-a865-5bb7e372fbf2">IVssWMComponent::GetComponentInfo</a> then 
    allocates and returns a <b>VSS_COMPONENTINFO</b> 
    structure.

Because <b>VSS_COMPONENTINFO</b> is allocated and 
    returned by 
    <a href="https://msdn.microsoft.com/ac01bfea-e60f-4f50-a865-5bb7e372fbf2">IVssWMComponent::GetComponentInfo</a>, 
    a requester should not free a <b>VSS_COMPONENTINFO</b> object 
    directly, but should use 
    <a href="https://msdn.microsoft.com/3f0c4634-2b1c-4a9b-9c13-ace38e03a7ce">IVssWMComponent::FreeComponentInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/fdbcbcea-d49e-49bc-9bb8-2210a9de02a4">IVssCreateWriterMetadata::AddComponent</a>



<a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a>



<a href="https://msdn.microsoft.com/fd03ac7c-8398-4972-85f1-2afe13317950">IVssExamineWriterMetadata::GetComponent</a>



<a href="https://msdn.microsoft.com/8567ca7f-dc50-4cf2-b3c1-a2ae8d55dc95">IVssWMComponent</a>



<a href="https://msdn.microsoft.com/3f0c4634-2b1c-4a9b-9c13-ace38e03a7ce">IVssWMComponent::FreeComponentInfo</a>



<a href="https://msdn.microsoft.com/ac01bfea-e60f-4f50-a865-5bb7e372fbf2">IVssWMComponent::GetComponentInfo</a>



<a href="https://msdn.microsoft.com/ba3b726c-448a-46c0-8fa5-5793497aa385">VSS_COMPONENT_TYPE</a>
 

 

