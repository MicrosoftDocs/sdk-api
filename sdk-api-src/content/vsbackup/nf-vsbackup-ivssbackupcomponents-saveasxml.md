---
UID: NF:vsbackup.IVssBackupComponents.SaveAsXML
title: IVssBackupComponents::SaveAsXML
author: windows-sdk-content
description: The SaveAsXML method saves the Backup Components Document containing a requester's state information to a specified string. This XML document, which contains the Backup Components Document, should always be securely saved as part of a backup operation.
old-location: base\ivssbackupcomponents_saveasxml.htm
old-project: vss
ms.assetid: 8184d15a-7d1f-49ed-afe3-fa9d81a4d32d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IVssBackupComponents interface [VSS],SaveAsXML method, IVssBackupComponents.SaveAsXML, IVssBackupComponents::SaveAsXML, SaveAsXML, SaveAsXML method [VSS], SaveAsXML method [VSS],IVssBackupComponents interface, _win32_ivssbackupcomponents_saveasxml, base.ivssbackupcomponents_saveasxml, vsbackup/IVssBackupComponents::SaveAsXML
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AMVPSIZE, *LPAMVPSIZE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssBackupComponents.SaveAsXML
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssBackupComponents::SaveAsXML


## -description


The 
<b>SaveAsXML</b> method saves the Backup Components Document containing a requester's state information to a specified string. This XML document, which contains the Backup Components Document, should always be securely saved as part of a backup operation.


## -parameters




### -param pbstrXML [in]

Pointer to a string to be used to store the Backup Components Document containing a requester's state information.


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
Successfully saved the XML document as the <i>pbstrXML</i> parameter value.

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



For a typical backup operation, 
<b>SaveAsXML</b> should not be called until after both writers and the requester are finished modifying the Backup Components Document.

Writers can continue to modify the Backup Components Document until their successful return from handling the PostSnapshot event (<a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">CVssWriter::OnPostSnapshot</a>), or equivalently upon the completion of 
<a href="https://msdn.microsoft.com/3cc6c375-8a24-4af3-b4ad-5a695cc2645c">IVssBackupComponents::DoSnapshotSet</a>.

Requesters will need to continue to modify the Backup Components Document as the backup progresses. In particular, a requester will store a component-by-component record of the success or failure of the backup through calls to the 
<a href="https://msdn.microsoft.com/5565183d-f374-4796-a399-b008041afdd2">IVssBackupComponents::SetBackupSucceeded</a> method.

Once the requester has finished modifying the Backup Components Document, the requester should use 
<b>SaveAsXML</b> to save a copy of the document to the backup media.

A Backup Components Document can be saved at earlier points in the life cycle of a backup operation—for instance, to support the generation of transportable shadow copies to be handled on remote machines. (See 
<a href="https://msdn.microsoft.com/4ec63917-03c0-434e-892e-3d9d4c47740e">Importing Transportable Shadow Copied Volumes</a> for more information.)

However, 
<b>SaveAsXML</b> should never be called prior to 
<a href="https://msdn.microsoft.com/46ce8282-a434-4b0b-b66e-40810052b34b">IVssBackupComponents::PrepareForBackup</a>, because the Backup Components Document will not have been filled by the requester and the writers.




## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/44f19c10-c966-4ab6-98dd-865d535955db">IVssBackupComponents::GatherWriterMetadata</a>



<a href="https://msdn.microsoft.com/df469964-c954-4f79-b88f-a521157a0c66">IVssBackupComponents::InitializeForBackup</a>



<a href="https://msdn.microsoft.com/a8ba1463-4da7-4539-8ade-b57ecda0a645">IVssBackupComponents::InitializeForRestore</a>



<a href="https://msdn.microsoft.com/46ce8282-a434-4b0b-b66e-40810052b34b">IVssBackupComponents::PrepareForBackup</a>
 

 

