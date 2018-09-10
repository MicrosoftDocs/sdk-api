---
UID: NF:vsbackup.IVssBackupComponents.GetWriterMetadata
title: IVssBackupComponents::GetWriterMetadata
author: windows-sdk-content
description: The GetWriterMetadata method returns the metadata for a specific writer running on the system.
old-location: base\ivssbackupcomponents_getwritermetadata.htm
tech.root: VSS
ms.assetid: a577d06a-4c9d-4ebe-b4d4-685f96ec9c83
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetWriterMetadata, GetWriterMetadata method [VSS], GetWriterMetadata method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],GetWriterMetadata method, IVssBackupComponents.GetWriterMetadata, IVssBackupComponents::GetWriterMetadata, _win32_ivssbackupcomponents_getwritermetadata, base.ivssbackupcomponents_getwritermetadata, vsbackup/IVssBackupComponents::GetWriterMetadata
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
 - IVssBackupComponents.GetWriterMetadata
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssBackupComponents::GetWriterMetadata


## -description


The 
<b>GetWriterMetadata</b> method returns the metadata for a specific writer running on the system.


## -parameters




### -param iWriter [in]

Index of the writer whose metadata is to be retrieved. The value of this parameter is an integer from 0 
      to <i>n</i>–1 inclusive, where <i>n</i> is the total number of writers on the current system. The value of <i>n</i> is returned by 
<a href="https://msdn.microsoft.com/cf8c4782-2850-4847-a7a1-95bd2bd547a1">IVssBackupComponents::GetWriterMetadataCount</a>.


### -param pidInstance

TBD


### -param ppMetadata [out]

Doubly indirect pointer to the instance of the 
<a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a> object that contains the returned metadata.


#### - pidWriterInstance [out]

Pointer to the instance identifier of the writer that collected the metadata.


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
Successfully returned a pointer to an 
<a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a> interface object.

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
The backup components object is not initialized, this method has been called during a restore operation, or this method has not been called within the correct sequence.

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
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified shadow copy does not exist.

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



A requester must call the asynchronous operation 
<a href="https://msdn.microsoft.com/44f19c10-c966-4ab6-98dd-865d535955db">IVssBackupComponents::GatherWriterMetadata</a> and wait for it to complete prior to calling <b>GetWriterMetadata</b>.

Although 
<a href="https://msdn.microsoft.com/44f19c10-c966-4ab6-98dd-865d535955db">IVssBackupComponents::GatherWriterMetadata</a> must be called prior to either a restore or backup operation, 
<b>GetWriterMetadata</b> is not typically called for restores.

Component information retrieved (during backup operations) using 
<a href="https://msdn.microsoft.com/fd03ac7c-8398-4972-85f1-2afe13317950">IVssExamineWriterMetadata::GetComponent</a>, where the 
<a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a> interface has been returned by 
<b>GetWriterMetadata</b>, comes from the Writer Metadata Document of a live writer process.

This is in contrast to the information returned by 
<a href="https://msdn.microsoft.com/b99e7e41-1c88-462c-b6d8-734f7a6e24d4">GetWriterComponents</a> (during restore operations), which was stored in the Backup Components Document by calls to 
<a href="https://msdn.microsoft.com/50cb0b16-9ed3-4496-962a-9c845c10986c">AddComponent</a>.

When the caller of this method is finished accessing the metadata, it must call <a href="_com_iunknown_release">IUnknown::Release</a>.




## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/50cb0b16-9ed3-4496-962a-9c845c10986c">IVssBackupComponents::AddComponent</a>



<a href="https://msdn.microsoft.com/44f19c10-c966-4ab6-98dd-865d535955db">IVssBackupComponents::GatherWriterMetadata</a>



<a href="https://msdn.microsoft.com/b99e7e41-1c88-462c-b6d8-734f7a6e24d4">IVssBackupComponents::GetWriterComponents</a>



<a href="https://msdn.microsoft.com/cf8c4782-2850-4847-a7a1-95bd2bd547a1">IVssBackupComponents::GetWriterMetadataCount</a>



<a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a>
 

 

