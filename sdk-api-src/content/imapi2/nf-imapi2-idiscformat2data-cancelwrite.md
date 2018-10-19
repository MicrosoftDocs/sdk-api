---
UID: NF:imapi2.IDiscFormat2Data.CancelWrite
title: IDiscFormat2Data::CancelWrite
author: windows-sdk-content
description: Cancels the current write operation.
old-location: imapi\idiscformat2data_cancelwrite.htm
tech.root: imapi
ms.assetid: 0fe5705e-7f48-4a4e-a535-a3dd105a6139
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CancelWrite, CancelWrite method [IMAPI], CancelWrite method [IMAPI],IDiscFormat2Data interface, IDiscFormat2Data interface [IMAPI],CancelWrite method, IDiscFormat2Data.CancelWrite, IDiscFormat2Data::CancelWrite, imapi.idiscformat2data_cancelwrite, imapi2/IDiscFormat2Data::CancelWrite
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
 - IDiscFormat2Data.CancelWrite
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscFormat2Data::CancelWrite


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



To cancel the write operation, you must call this method from the <a href="https://msdn.microsoft.com/786fc936-9493-4cc3-a937-4d1f4b54fe88">DDiscFormat2DataEvents::Update</a> event handler that you implemented. 

Note that calling this method does not immediately cancel the write operation on all media due to media-specific requirements. For example, when writing to a CD, the write operation can continue for up to three more minutes.

This method leaves the media in an indeterminate state. For rewriteable media, you should call the <a href="https://msdn.microsoft.com/dc71d1bf-b068-42c0-a87d-ae8fac279a58">IDiscFormat2Erase::EraseMedia</a> method after calling this method to prepare the media for future use.




## -see-also




<a href="https://msdn.microsoft.com/697f8247-6940-4b5e-8521-df89838837be">DWriteEngine2Events</a>



<a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a>



<a href="https://msdn.microsoft.com/9daf31f3-84c2-48b2-ab21-a3809b6ed9af">IDiscFormat2Data::Write</a>
 

 

