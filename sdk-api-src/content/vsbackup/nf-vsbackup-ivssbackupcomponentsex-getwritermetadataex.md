---
UID: NF:vsbackup.IVssBackupComponentsEx.GetWriterMetadataEx
title: IVssBackupComponentsEx::GetWriterMetadataEx (vsbackup.h)
description: The GetWriterMetadataEx method returns the metadata for a specific writer instance running on the system.helpviewer_keywords: ["GetWriterMetadataEx","GetWriterMetadataEx method [VSS]","GetWriterMetadataEx method [VSS]","IVssBackupComponentsEx interface","IVssBackupComponentsEx interface [VSS]","GetWriterMetadataEx method","IVssBackupComponentsEx.GetWriterMetadataEx","IVssBackupComponentsEx::GetWriterMetadataEx","base.ivssbackupcomponentsex_getwritermetadataex","vsbackup/IVssBackupComponentsEx::GetWriterMetadataEx"]
old-location: base\ivssbackupcomponentsex_getwritermetadataex.htm
tech.root: VSS
ms.assetid: 19a31627-54e0-4b0d-87cf-ac18b3049310
ms.date: 12/05/2018
ms.keywords: GetWriterMetadataEx, GetWriterMetadataEx method [VSS], GetWriterMetadataEx method [VSS],IVssBackupComponentsEx interface, IVssBackupComponentsEx interface [VSS],GetWriterMetadataEx method, IVssBackupComponentsEx.GetWriterMetadataEx, IVssBackupComponentsEx::GetWriterMetadataEx, base.ivssbackupcomponentsex_getwritermetadataex, vsbackup/IVssBackupComponentsEx::GetWriterMetadataEx
f1_keywords:
- vsbackup/IVssBackupComponentsEx.GetWriterMetadataEx
dev_langs:
- c++
req.header: vsbackup.h
req.include-header: VsBackup.h, Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
- IVssBackupComponentsEx.GetWriterMetadataEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssBackupComponentsEx::GetWriterMetadataEx


## -description


The 
<b>GetWriterMetadataEx</b> method returns the metadata for a specific writer instance running on the system.


## -parameters




### -param iWriter [in]

Index of the writer whose metadata is to be retrieved. The value of this parameter is an integer from 0 
      to <i>n</i>–1 inclusive, where <i>n</i> is the total number of writers on the current system. The value of <i>n</i> is returned by 
the <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount">IVssBackupComponents::GetWriterMetadataCount</a> method.


### -param pidInstance [out]

Address of a caller-allocated variable that receives the instance identifier of the writer that collected the metadata.


### -param ppMetadata [out]

Doubly indirect pointer to the instance of the 
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadataex">IVssExamineWriterMetadataEx</a> object that contains the returned metadata.


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
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadataex">IVssExamineWriterMetadataEx</a> interface object.

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
<a href="https://docs.microsoft.com/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The <i>iWriter</i> parameter does not point to a valid writer.

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
        <a href="https://docs.microsoft.com/windows/desktop/VSS/event-and-error-handling-under-vss">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>
 




## -remarks



<b>GetWriterMetadataEx</b> is identical to the <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata">IVssBackupComponents::GetWriterMetadata</a> method, except that it returns an <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadataex">IVssExamineWriterMetadataEx</a> interface pointer instead of an <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a> interface pointer in the <i>ppMetadata</i> parameter.

A requester must call the asynchronous <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata">IVssBackupComponents::GatherWriterMetadata</a> method and wait for it to complete prior to calling <b>GetWriterMetadataEx</b>.

Although 
the <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata">GatherWriterMetadata</a> method must be called prior to either a restore or backup operation, 
<b>GetWriterMetadataEx</b> is not typically called for restores.

Component information retrieved (during backup operations) using 
the <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent">IVssExamineWriterMetadata::GetComponent</a> method, where the 
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadataex">IVssExamineWriterMetadataEx</a> interface has been returned by 
<b>GetWriterMetadataEx</b>, comes from the Writer Metadata Document of a live writer process.

This is in contrast to the information returned by 
<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents">GetWriterComponents</a> (during restore operations), which was stored in the Backup Components Document by calls to 
the <a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-addcomponent">IVssBackupComponents::AddComponent</a> method.

When the caller of this method is finished accessing the metadata, it must call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata">IVssBackupComponents::GetWriterMetadata</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssbackupcomponentsex">IVssBackupComponentsEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadata">IVssExamineWriterMetadata</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vsbackup/nl-vsbackup-ivssexaminewritermetadataex">IVssExamineWriterMetadataEx</a>
 

 

