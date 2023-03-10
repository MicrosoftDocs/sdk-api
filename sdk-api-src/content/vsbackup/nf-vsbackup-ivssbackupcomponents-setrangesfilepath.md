---
UID: NF:vsbackup.IVssBackupComponents.SetRangesFilePath
title: IVssBackupComponents::SetRangesFilePath (vsbackup.h)
description: The SetRangesFilePath method is used when a partial file operation requires a ranges file, and that file has been restored to a location other than its original one.
helpviewer_keywords: ["IVssBackupComponents interface [VSS]","SetRangesFilePath method","IVssBackupComponents.SetRangesFilePath","IVssBackupComponents::SetRangesFilePath","SetRangesFilePath","SetRangesFilePath method [VSS]","SetRangesFilePath method [VSS]","IVssBackupComponents interface","_win32_ivssbackupcomponents_setrangesfilepath","base.ivssbackupcomponents_setrangesfilepath","vsbackup/IVssBackupComponents::SetRangesFilePath"]
old-location: base\ivssbackupcomponents_setrangesfilepath.htm
tech.root: base
ms.assetid: 170f9ea0-4846-49d4-ab06-eb1ce580e827
ms.date: 12/05/2018
ms.keywords: IVssBackupComponents interface [VSS],SetRangesFilePath method, IVssBackupComponents.SetRangesFilePath, IVssBackupComponents::SetRangesFilePath, SetRangesFilePath, SetRangesFilePath method [VSS], SetRangesFilePath method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_setrangesfilepath, base.ivssbackupcomponents_setrangesfilepath, vsbackup/IVssBackupComponents::SetRangesFilePath
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssBackupComponents::SetRangesFilePath
 - vsbackup/IVssBackupComponents::SetRangesFilePath
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
 - IVssBackupComponents.SetRangesFilePath
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
<a href="/windows/desktop/api/vswriter/ne-vswriter-vss_component_type">VSS_COMPONENT_TYPE</a> for possible return values.

### -param wszLogicalPath [in]

<b>Null</b>-terminated wide character string containing the logical path of the component containing the files that are participating in the partial file operation. 


For more information, see <a href="/windows/desktop/VSS/logical-pathing-of-components">Logical Pathing of Components</a>.

The value of the string containing the logical path used here should be the same as was used when the component was added to the backup set using 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>.

The logical path can be <b>NULL</b>.

There are no restrictions on the characters that can appear in a non-<b>NULL</b> logical path.

### -param wszComponentName [in]

<b>Null</b>-terminated wide character string containing the name of the component containing the files that are participating in the partial file operation. 




The string cannot be <b>NULL</b> and should contain the same component name as was used when the component was added to the backup set using 
<a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a>.

### -param iPartialFile [in]

Index number of the partial file. The value of this parameter is an integer from 0 
      to <i>n</i>–1 inclusive, where <i>n</i> is the total number of partial files associated with a given component. The value of <i>n</i> is returned by 
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getpartialfilecount">IVssComponent::GetPartialFileCount</a>.

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
<a href="/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

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

Calling 
<b>SetRangesFilePath</b> is not necessary if ranges files are restored in place.

## -see-also

<a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponents">IVssBackupComponents</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-addpartialfile">IVssComponent::AddPartialFile</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getpartialfile">IVssComponent::GetPartialFile</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getpartialfilecount">IVssComponent::GetPartialFileCount</a>