---
UID: NF:vsbackup.IVssBackupComponents.SetRestoreOptions
title: IVssBackupComponents::SetRestoreOptions method
author: windows-driver-content
description: The SetRestoreOptions method sets a string of private, or writer-dependent, restore parameters for a writer component.
old-location: base\ivssbackupcomponents_setrestoreoptions.htm
old-project: VSS
ms.assetid: 4a872594-dcd8-463d-9f6b-6bc40c17df38
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: IVssBackupComponents, IVssBackupComponents interface [VSS], SetRestoreOptions method, IVssBackupComponents::SetRestoreOptions, SetRestoreOptions method [VSS], SetRestoreOptions method [VSS], IVssBackupComponents interface, SetRestoreOptions,IVssBackupComponents.SetRestoreOptions, _win32_ivssbackupcomponents_setrestoreoptions, base.ivssbackupcomponents_setrestoreoptions, vsbackup/IVssBackupComponents::SetRestoreOptions
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
-	IVssBackupComponents.SetRestoreOptions
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssBackupComponents::SetRestoreOptions method


## -description


The <b>SetRestoreOptions</b> method 
    sets a string of private, or writer-dependent, restore parameters for a writer component.


## -parameters




### -param writerId [in]

Writer identifier.


### -param ct




### -param wszLogicalPath [in]

Null-terminated wide character string containing the logical path of the component. 
      For more information, see <a href="https://msdn.microsoft.com/663c8ca9-8f5b-48bd-af2d-b2d90de9e492">Logical Pathing of Components</a>.

The value of the string containing the logical path used here should be the same as was used when the 
       component was added to the backup set using 
       <a href="https://msdn.microsoft.com/50cb0b16-9ed3-4496-962a-9c845c10986c">IVssBackupComponents::AddComponent</a>.

The logical path can be <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-NULL logical path.


### -param wszComponentName [in]

Null-terminated wide character string containing the name of the component. 
      

The string cannot be <b>NULL</b> and should contain the same component name as was used when the component was added 
      to the backup set using 
      <a href="https://msdn.microsoft.com/50cb0b16-9ed3-4496-962a-9c845c10986c">IVssBackupComponents::AddComponent</a>.


### -param wszRestoreOptions [in]

Null-terminated wide character string containing the private string of restore parameters. For more 
      information see <a href="https://msdn.microsoft.com/364550a1-070a-4f7e-bd62-84672959dc21">Setting VSS Restore 
      Options</a>.


#### - componentType [in]

Type of the component. See <a href="https://msdn.microsoft.com/ba3b726c-448a-46c0-8fa5-5793497aa385">VSS_COMPONENT_TYPE</a> 
      for the possible values.


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
Successfully set the previous backup time stamp.

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
The XML document is not valid. Check the event log for details. For more 
        information, see 
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



This method must be called before 
    <a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">IVssBackupComponents::PreRestore</a>.

The exact syntax and content of the restore options set by the <i>wszRestoreOptions</i> 
    parameter of the 
    <b>SetRestoreOptions</b> method will 
    depend on the specific writer being contacted.




## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">IVssBackupComponents::PreRestore</a>



<a href="https://msdn.microsoft.com/ba3b726c-448a-46c0-8fa5-5793497aa385">VSS_COMPONENT_TYPE</a>
 

 

