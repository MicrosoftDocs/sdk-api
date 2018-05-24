---
UID: NF:vsbackup.IVssBackupComponents.SetRangesFilePath
title: IVssBackupComponents::SetRangesFilePath
author: windows-driver-content
description: The SetRangesFilePath method is used when a partial file operation requires a ranges file, and that file has been restored to a location other than its original one.
old-location: base\ivssbackupcomponents_setrangesfilepath.htm
old-project: VSS
ms.assetid: 170f9ea0-4846-49d4-ab06-eb1ce580e827
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IVssBackupComponents interface [VSS],SetRangesFilePath method, IVssBackupComponents.SetRangesFilePath, IVssBackupComponents::SetRangesFilePath, SetRangesFilePath, SetRangesFilePath method [VSS], SetRangesFilePath method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_setrangesfilepath, base.ivssbackupcomponents_setrangesfilepath, vsbackup/IVssBackupComponents::SetRangesFilePath
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
-	IVssBackupComponents.SetRangesFilePath
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssBackupComponents::SetRangesFilePath


## -description


The 
<b>SetRangesFilePath</b> method is used when a partial file operation requires a ranges file, and that file has been restored to a location other than its original one.


## -parameters




### -param writerId [in]

Globally unique identifier (GUID) of the writer class containing the files involved in the partial file operation.


### -param ct [in]

Identifies the type of the component. Refer to 
<a href="https://msdn.microsoft.com/ba3b726c-448a-46c0-8fa5-5793497aa385">VSS_COMPONENT_TYPE</a> for possible return values.


### -param wszLogicalPath [in]

<b>Null</b>-terminated wide character string containing the logical path of the component containing the files that are participating in the partial file operation. 


For more information, see <a href="https://msdn.microsoft.com/663c8ca9-8f5b-48bd-af2d-b2d90de9e492">Logical Pathing of Components</a>.

The value of the string containing the logical path used here should be the same as was used when the component was added to the backup set using 
<a href="https://msdn.microsoft.com/50cb0b16-9ed3-4496-962a-9c845c10986c">IVssBackupComponents::AddComponent</a>.

The logical path can be <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-<b>NULL</b> logical path.


### -param wszComponentName [in]

<b>Null</b>-terminated wide character string containing the name of the component containing the files that are participating in the partial file operation. 




The string cannot be <b>NULL</b> and should contain the same component name as was used when the component was added to the backup set using 
<a href="https://msdn.microsoft.com/50cb0b16-9ed3-4496-962a-9c845c10986c">IVssBackupComponents::AddComponent</a>.


### -param iPartialFile [in]

Index number of the partial file. The value of this parameter is an integer from 0 
      to <i>n</i>–1 inclusive, where <i>n</i> is the total number of partial files associated with a given component. The value of <i>n</i> is returned by 
<a href="https://msdn.microsoft.com/7be84c00-49c4-4c44-9c12-7994247726a5">IVssComponent::GetPartialFileCount</a>.


### -param wszRangesFile [in]

<b>Null</b>-terminated wide character string containing the fully qualified path of a ranges file.


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
Successfully added the new restore target.

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
The backup components object is not initialized, or this method has been called other than during a restore operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The component does not exist or the path and file specification do not match a component and file specification in the component.

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



Calling 
<b>SetRangesFilePath</b> is not necessary if ranges files are restored in place.




## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/318dc1ee-e63f-4e79-96b9-8a8bd83facd3">IVssComponent::AddPartialFile</a>



<a href="https://msdn.microsoft.com/ed589ae8-2abb-4c3b-9695-12649fc89818">IVssComponent::GetPartialFile</a>



<a href="https://msdn.microsoft.com/7be84c00-49c4-4c44-9c12-7994247726a5">IVssComponent::GetPartialFileCount</a>
 

 

