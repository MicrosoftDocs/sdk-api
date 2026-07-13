---
UID: NF:imapi2.IDiscFormat2Data.CancelWrite
title: IDiscFormat2Data::CancelWrite (imapi2.h)
description: Cancels the current write operation. (IDiscFormat2Data.CancelWrite)
helpviewer_keywords: ["CancelWrite","CancelWrite method [IMAPI]","CancelWrite method [IMAPI]","IDiscFormat2Data interface","IDiscFormat2Data interface [IMAPI]","CancelWrite method","IDiscFormat2Data.CancelWrite","IDiscFormat2Data::CancelWrite","imapi.idiscformat2data_cancelwrite","imapi2/IDiscFormat2Data::CancelWrite"]
old-location: imapi\idiscformat2data_cancelwrite.htm
tech.root: imapi
ms.assetid: 0fe5705e-7f48-4a4e-a535-a3dd105a6139
ms.date: 12/05/2018
ms.keywords: CancelWrite, CancelWrite method [IMAPI], CancelWrite method [IMAPI],IDiscFormat2Data interface, IDiscFormat2Data interface [IMAPI],CancelWrite method, IDiscFormat2Data.CancelWrite, IDiscFormat2Data::CancelWrite, imapi.idiscformat2data_cancelwrite, imapi2/IDiscFormat2Data::CancelWrite
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiscFormat2Data::CancelWrite
 - imapi2/IDiscFormat2Data::CancelWrite
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscFormat2Data.CancelWrite
---

# IDiscFormat2Data::CancelWrite


## -description

Cancels the current write operation.



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
<dt><b>E_IMAPI_DF2DATA_WRITE_NOT_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
There is no write operation currently in progress.

Value: 0xC0AA0401

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified failure.

Value: 0x80004005

</td>
</tr>
</table>

## -remarks

To cancel the write operation, you must call this method from the <a href="/windows/desktop/api/imapi2/nf-imapi2-ddiscformat2dataevents-update">DDiscFormat2DataEvents::Update</a> event handler that you implemented. 

Note that calling this method does not immediately cancel the write operation on all media due to media-specific requirements. For example, when writing to a CD, the write operation can continue for up to three more minutes.

This method leaves the media in an indeterminate state. For rewriteable media, you should call the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2erase-erasemedia">IDiscFormat2Erase::EraseMedia</a> method after calling this method to prepare the media for future use.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events">DWriteEngine2Events</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write">IDiscFormat2Data::Write</a>
