---
UID: NF:bdatif.ITuneRequestInfo.GetNextProgram
title: ITuneRequestInfo::GetNextProgram
author: windows-sdk-content
description: The GetNextProgram method creates a new tune request with channel or program locator information for the next service.
old-location: mstv\itunerequestinfo_getnextprogram.htm
tech.root: MSTV
ms.assetid: ed1c5a30-19fb-46a8-b521-017da56d85c8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetNextProgram, GetNextProgram method [Microsoft TV Technologies], GetNextProgram method [Microsoft TV Technologies],ITuneRequestInfo interface, ITuneRequestInfo interface [Microsoft TV Technologies],GetNextProgram method, ITuneRequestInfo.GetNextProgram, ITuneRequestInfo::GetNextProgram, ITuneRequestInfoGetNextProgram, bdatif/ITuneRequestInfo::GetNextProgram, mstv.itunerequestinfo_getnextprogram
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: bdatif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - bdatif.h
api_name:
 - ITuneRequestInfo.GetNextProgram
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- bdatif.h
: 
- ITuneRequestInfo.GetNextProgram
: 
---

# ITuneRequestInfo::GetNextProgram


## -description



The <b>GetNextProgram</b> method creates a new tune request with channel or program locator information for the next service.




## -parameters




### -param CurrentRequest

TBD


### -param TuneRequest

TBD




#### - pCurrentRequest [in]

Specifies the <a href="https://msdn.microsoft.com/en-us/library/Dd694997(v=VS.85).aspx">ITuneRequest</a> interface of the current request.


#### - ppTuneRequest [out]

Pointer to a variable that will receive a tune request for the next service on the transport stream.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>CurrentRequest</i> is not valid, or <i>TuneRequest</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method might be used by a custom Guide Store Loader to enumerate the available services on a transport stream.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694998(v=VS.85).aspx">ITuneRequestInfo Interface</a>
 

 

