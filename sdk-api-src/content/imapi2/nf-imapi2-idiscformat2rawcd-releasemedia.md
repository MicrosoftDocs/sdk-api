---
UID: NF:imapi2.IDiscFormat2RawCD.ReleaseMedia
title: IDiscFormat2RawCD::ReleaseMedia (imapi2.h)
description: Closes a Disc-At-Once (DAO) writing session of a raw image and releases the lock.helpviewer_keywords: ["IDiscFormat2RawCD interface [IMAPI]","ReleaseMedia method","IDiscFormat2RawCD.ReleaseMedia","IDiscFormat2RawCD::ReleaseMedia","ReleaseMedia","ReleaseMedia method [IMAPI]","ReleaseMedia method [IMAPI]","IDiscFormat2RawCD interface","imapi.idiscformat2rawcd_releasemedia","imapi2/IDiscFormat2RawCD::ReleaseMedia"]
old-location: imapi\idiscformat2rawcd_releasemedia.htm
tech.root: imapi
ms.assetid: 5f60c16f-ef40-4bb5-8df2-fa4ae91541b6
ms.date: 12/05/2018
ms.keywords: IDiscFormat2RawCD interface [IMAPI],ReleaseMedia method, IDiscFormat2RawCD.ReleaseMedia, IDiscFormat2RawCD::ReleaseMedia, ReleaseMedia, ReleaseMedia method [IMAPI], ReleaseMedia method [IMAPI],IDiscFormat2RawCD interface, imapi.idiscformat2rawcd_releasemedia, imapi2/IDiscFormat2RawCD::ReleaseMedia
f1_keywords:
- imapi2/IDiscFormat2RawCD.ReleaseMedia
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- imapi2.h
api_name:
- IDiscFormat2RawCD.ReleaseMedia
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



This method release the lock set when you called the <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-preparemedia">IDiscFormat2RawCD::PrepareMedia</a> method. You must call this method after the write operation completes or after calling <a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-cancelwrite">IDiscFormat2RawCD::CancelWrite</a> to cancel a writing operation.  




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd">IDiscFormat2RawCD</a>



IDiscFormat2RawCD::CancelWrite



<a href="https://docs.microsoft.com/windows/desktop/api/imapi2/nf-imapi2-idiscformat2rawcd-preparemedia">IDiscFormat2RawCD::PrepareMedia</a>
 

 

