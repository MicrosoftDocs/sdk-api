---
UID: NF:imapi2.IDiscFormat2RawCD.ReleaseMedia
title: IDiscFormat2RawCD::ReleaseMedia
author: windows-driver-content
description: Closes a Disc-At-Once (DAO) writing session of a raw image and releases the lock.
old-location: imapi\idiscformat2rawcd_releasemedia.htm
old-project: imapi
ms.assetid: 5f60c16f-ef40-4bb5-8df2-fa4ae91541b6
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IDiscFormat2RawCD interface [IMAPI],ReleaseMedia method, IDiscFormat2RawCD.ReleaseMedia, IDiscFormat2RawCD::ReleaseMedia, ReleaseMedia, ReleaseMedia method [IMAPI], ReleaseMedia method [IMAPI],IDiscFormat2RawCD interface, imapi.idiscformat2rawcd_releasemedia, imapi2/IDiscFormat2RawCD::ReleaseMedia
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2.h
api_name:
-	IDiscFormat2RawCD.ReleaseMedia
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscFormat2RawCD::ReleaseMedia


## -description


Closes a Disc-At-Once (DAO) writing session of a raw image and releases the lock.


## -parameters






## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2RAW_MEDIA_IS_NOT_PREPARED</b></dt>
</dl>
</td>
<td width="60%">
The requested operation is only valid when media has been "prepared".

Value: 0xC0AA0602

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_IMAPI_DF2RAW_WRITE_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
There is currently a write operation in progress.

Value: 0xC0AA0600

</td>
</tr>
</table>
 




## -remarks



This method release the lock set when you called the <a href="https://msdn.microsoft.com/8c393786-0c2d-4244-8ec3-0ac9e47e76c6">IDiscFormat2RawCD::PrepareMedia</a> method. You must call this method after the write operation completes or after calling <a href="https://msdn.microsoft.com/12cd6797-dcb8-496d-a141-9d3a805266e9">IDiscFormat2RawCD::CancelWrite</a> to cancel a writing operation.  




## -see-also




<a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a>



IDiscFormat2RawCD::CancelWrite



<a href="https://msdn.microsoft.com/8c393786-0c2d-4244-8ec3-0ac9e47e76c6">IDiscFormat2RawCD::PrepareMedia</a>
 

 

