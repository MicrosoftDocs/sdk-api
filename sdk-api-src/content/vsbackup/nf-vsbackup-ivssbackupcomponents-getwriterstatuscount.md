---
UID: NF:vsbackup.IVssBackupComponents.GetWriterStatusCount
title: IVssBackupComponents::GetWriterStatusCount
author: windows-driver-content
description: The GetWriterStatusCount method returns the number of writers with status.
old-location: base\ivssbackupcomponents_getwriterstatuscount.htm
old-project: VSS
ms.assetid: e358cb2b-9b0f-47fb-a0ca-7bbbc6e49aff
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetWriterStatusCount, GetWriterStatusCount method [VSS], GetWriterStatusCount method [VSS],IVssBackupComponents interface, IVssBackupComponents interface [VSS],GetWriterStatusCount method, IVssBackupComponents.GetWriterStatusCount, IVssBackupComponents::GetWriterStatusCount, _win32_ivssbackupcomponents_getwriterstatuscount, base.ivssbackupcomponents_getwriterstatuscount, vsbackup/IVssBackupComponents::GetWriterStatusCount
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
-	IVssBackupComponents.GetWriterStatusCount
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssBackupComponents::GetWriterStatusCount


## -description


The 
<b>GetWriterStatusCount</b> method returns the number of writers with status.


## -parameters




### -param pcWriters [out]

The number of writers with status.


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
Successfully returned the number of writers with status.

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



A requester must call the asynchronous operation 
<a href="https://msdn.microsoft.com/ca87cdc3-e233-4efc-81c0-918e5a698af5">IVssBackupComponents::GatherWriterStatus</a> and wait for it to complete prior to calling <b>IVssBackupComponents::GetWriterStatusCount</b>.

The number of writers returned by 
<b>GetWriterStatusCount</b> should always be the same as that returned by 
<a href="https://msdn.microsoft.com/cf8c4782-2850-4847-a7a1-95bd2bd547a1">IVssBackupComponents::GetWriterMetadataCount</a>.




## -see-also




<a href="https://msdn.microsoft.com/fe1220c7-11e5-4872-b7a9-61558f7c75c0">IVssBackupComponents</a>



<a href="https://msdn.microsoft.com/ca87cdc3-e233-4efc-81c0-918e5a698af5">IVssBackupComponents::GatherWriterStatus</a>



<a href="https://msdn.microsoft.com/652e9630-291d-41cd-96d9-6a63988932a5">IVssBackupComponents::GetWriterStatus</a>



<a href="https://msdn.microsoft.com/97aa20a3-4d58-49e8-83c0-fc33c700c410">VSS_WRITER_STATE</a>
 

 

