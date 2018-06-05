---
UID: NF:imapi2.IDiscFormat2RawCD.CancelWrite
title: IDiscFormat2RawCD::CancelWrite
author: windows-sdk-content
description: Cancels the current write operation.
old-location: imapi\idiscformat2rawcd_cancelwrite.htm
old-project: imapi
ms.assetid: 12cd6797-dcb8-496d-a141-9d3a805266e9
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CancelWrite, CancelWrite method [IMAPI], CancelWrite method [IMAPI],IDiscFormat2RawCD interface, IDiscFormat2RawCD interface [IMAPI],CancelWrite method, IDiscFormat2RawCD.CancelWrite, IDiscFormat2RawCD::CancelWrite, imapi.idiscformat2rawcd_cancelwrite, imapi2/IDiscFormat2RawCD::CancelWrite
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2.h
api_name:
-	IDiscFormat2RawCD.CancelWrite
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscFormat2RawCD::CancelWrite


## -description


Cancels the current write operation.


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
<dt><b>E_IMAPI_DF2RAW_WRITE_NOT_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
There is no write operation currently in progress.

Value: 0xC0AA0601

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



To cancel the write operation, you must call this method from the <a href="https://msdn.microsoft.com/abe35eee-63a4-4109-8927-825f86b6e302">DDiscFormat2RawCDEvents::Update</a> event handler that you implemented. 

You must also call the <a href="https://msdn.microsoft.com/5f60c16f-ef40-4bb5-8df2-fa4ae91541b6">IDiscFormat2RawCD::ReleaseMedia</a> method after calling this method.

Note that calling this method does not immediately cancel the write operation on all media due to media-specific requirements. For example, when writing to a CD, the write operation can continue for up to three more minutes.

This method leaves the media in an indeterminate state. For rewriteable media, you should call the <a href="https://msdn.microsoft.com/dc71d1bf-b068-42c0-a87d-ae8fac279a58">IDiscFormat2Erase::EraseMedia</a> method after calling this method to prepare the media for future use.




## -see-also




<a href="https://msdn.microsoft.com/abe35eee-63a4-4109-8927-825f86b6e302">DDiscFormat2RawCDEvents::Update</a>



<a href="https://msdn.microsoft.com/58d9b83c-a528-4b39-b08d-a0fb8c1aece8">IDiscFormat2RawCD</a>
 

 

