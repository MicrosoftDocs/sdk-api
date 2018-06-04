---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IVssCreateWriterMetadata::AddComponent


## -description



    The <b>AddComponent</b> method adds a 
    database or file group as a component to be backed up.


## -parameters




### -param ct




### -param wszLogicalPath [in]

A pointer to a <b>null</b>-terminated wide character string containing the logical path of the database or file group. 
      For more information, see <a href="https://msdn.microsoft.com/663c8ca9-8f5b-48bd-af2d-b2d90de9e492">Logical Pathing of Components</a>.

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
      <a href="vssgloss_e.htm">explicitly included</a> in 
      the backup document. If the component was explicitly added to the backup document, it can always be 
      individually selected for restore; in this case, this flag has no meaning. 
      


       When <b>true</b>, the component can be restored by itself; when <b>false</b>, the component can be restored only if 
       the entire component set is being restored. (See 
       <a href="https://msdn.microsoft.com/9723e90e-cd5e-4815-843b-8ed8632ebe45">VSS_COMPONENTINFO</a> and 
       <a href="https://msdn.microsoft.com/e8920cca-d944-437f-bf6a-7ce8d518746a">Working with Selectability 
       and Logical Paths</a> for more information).
      

The default value for this parameter is <b>false</b>.


### -param dwComponentFlags [in]


      A bit mask (or bitwise OR) of members of the 
      <a href="https://msdn.microsoft.com/91b7fbab-82f8-48cc-8078-f8f71c48a70b">VSS_COMPONENT_FLAGS</a> enumeration indicating the features that this component supports. 
      

The default value for this argument is zero.


#### - componentType [in]


      A <a href="https://msdn.microsoft.com/ba3b726c-448a-46c0-8fa5-5793497aa385">VSS_COMPONENT_TYPE</a> enumeration value specifying 
      the type of the component.

<b>Windows Server 2003 and Windows XP:  </b>Before Windows Server 2003 with SP1, this parameter is reserved for system use, and the caller should not override the default value.


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
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

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
    <a href="https://msdn.microsoft.com/684dc50f-5d7b-4c95-85dd-77c320d65fff">Working with 
    Selectability for Restore and Subcomponents</a> for more information.
   




## -see-also




<a href="https://msdn.microsoft.com/427ed302-c3b7-483a-aa48-da6fec1160a9">IVssCreateWriterMetadata</a>
 

 

