---
UID: NF:vswriter.IVssCreateWriterMetadata.AddComponent
title: IVssCreateWriterMetadata::AddComponent (vswriter.h)
description: The AddComponent method adds a database or file group as a component to be backed up.
helpviewer_keywords: ["AddComponent","AddComponent method [VSS]","AddComponent method [VSS]","IVssCreateWriterMetadata interface","IVssCreateWriterMetadata interface [VSS]","AddComponent method","IVssCreateWriterMetadata.AddComponent","IVssCreateWriterMetadata::AddComponent","_win32_ivsscreatewritermetadata_addcomponent","base.ivsscreatewritermetadata_addcomponent","vswriter/IVssCreateWriterMetadata::AddComponent"]
old-location: base\ivsscreatewritermetadata_addcomponent.htm
tech.root: base
ms.assetid: fdbcbcea-d49e-49bc-9bb8-2210a9de02a4
ms.date: 12/05/2018
ms.keywords: AddComponent, AddComponent method [VSS], AddComponent method [VSS],IVssCreateWriterMetadata interface, IVssCreateWriterMetadata interface [VSS],AddComponent method, IVssCreateWriterMetadata.AddComponent, IVssCreateWriterMetadata::AddComponent, _win32_ivsscreatewritermetadata_addcomponent, base.ivsscreatewritermetadata_addcomponent, vswriter/IVssCreateWriterMetadata::AddComponent
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssCreateWriterMetadata::AddComponent
 - vswriter/IVssCreateWriterMetadata::AddComponent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssCreateWriterMetadata.AddComponent
---

# IVssCreateWriterMetadata::AddComponent


## -description

The <b>AddComponent</b> method adds a 
    database or file group as a component to be backed up.

## -parameters

### -param ct [in]

A <a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a> enumeration value specifying 
      the type of the component.

<b>Windows Server 2003 and Windows XP:  </b>Before Windows Server 2003 with SP1, this parameter is reserved for system use, and the caller should not override the default value.

### -param wszLogicalPath [in]

A pointer to a <b>null</b>-terminated wide character string containing the logical path of the database or file group. 
      For more information, see <a href="/windows/desktop/VSS/logical-pathing-of-components">Logical Pathing of Components</a>.

A logical path is optional and can be <b>NULL</b>.

### -param wszComponentName [in]

A pointer to a <b>null</b>-terminated wide character string containing the name of the component. This string is not localized. 
      

This parameter is required and cannot be <b>NULL</b>. The string cannot contain backslashes.

### -param wszCaption [in]

A pointer to a <b>null</b>-terminated wide character string containing a description (also called a "friendly name") for the component. 
      This string might be localized, and therefore requesters must assume that it is localized. 

This parameter is optional and can be <b>NULL</b>. The string can contain backslashes.

### -param pbIcon [in]

A pointer to a bitmap of the icon representing the database, to be displayed in a user interface. 
      The size, in bytes, of the buffer is specified by the <i>cbIcon</i> parameter. 
      

If the writer does not want to specify an icon, <i>pbIcon</i> should be set to <b>NULL</b>.

### -param cbIcon [in]

The size, in bytes, of the buffer. If 
     the <i>pbIcon</i> parameter is <b>NULL</b>, 
     <i>cbIcon</i> should be zero.

### -param bRestoreMetadata [in]

This parameter is reserved for future use and should always be set to <b>false</b>.

### -param bNotifyOnBackupComplete [in]

This parameter is reserved for future use and should always be set to <b>false</b>.

### -param bSelectable [in]

A Boolean that indicates whether the component can be optionally backed up (which means it can be excluded
      from the backup) or is always backed up when any of the writer's component is backed up. The Boolean is 
      <b>true</b> if the component can be selectively backed up and <b>false</b> if it is backed up when any of the components 
      is backed up.

### -param bSelectableForRestore [in]

A Boolean that determines whether a component can be individually restored when it has not been 
      <a href="/windows/desktop/VSS/vssgloss-e">explicitly included</a> in 
      the backup document. If the component was explicitly added to the backup document, it can always be 
      individually selected for restore; in this case, this flag has no meaning. 
      

When <b>true</b>, the component can be restored by itself; when <b>false</b>, the component can be restored only if 
       the entire component set is being restored. (See 
       <a href="/windows/desktop/api/vsbackup/ns-vsbackup-vss_componentinfo">VSS_COMPONENTINFO</a> and 
       <a href="/windows/desktop/VSS/working-with-selectability-and-logical-paths">Working with Selectability 
       and Logical Paths</a> for more information).
      

The default value for this parameter is <b>false</b>.

### -param dwComponentFlags [in]

A bit mask (or bitwise OR) of members of the 
      <a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_flags">VSS_COMPONENT_FLAGS</a> enumeration indicating the features that this component supports. 
      

The default value for this argument is zero.

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
The operation was successful.

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
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. 
        For more information, see 
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The object is a duplicate. A component with the same logical path and component name already exists.

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
        <a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>

## -remarks

This method can be called multiple times to add several components to a writer's metadata.

The combination of logical path and name for each component of a given instance of a given class of writer 
    must be unique. Attempting to call 
    <b>AddComponent</b> twice with 
    the same values of <i>wszLogicalPath</i> and <i>wszComponentName</i> results 
    in a VSS_E_OBJECT_ALREADY_EXISTS error.

<b>AddComponent</b> can be used to 
    add subcomponents—components in which all member files are backed up as a group, but which contain 
    files that can be restored individually. See 
    <a href="/windows/desktop/VSS/working-with-selectability-for-restore-and-subcomponents">Working with 
    Selectability for Restore and Subcomponents</a> for more information.

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscreatewritermetadata">IVssCreateWriterMetadata</a>