---
UID: NF:bdatif.ITuneRequestInfo.GetPreviousLocator
title: ITuneRequestInfo::GetPreviousLocator
author: windows-sdk-content
description: The GetPreviousLocator method creates a new tune request with locator information for the previous transport stream.
old-location: mstv\itunerequestinfo_getpreviouslocator.htm
tech.root: mstv
ms.assetid: 72512da5-28d4-40b8-93df-039014f432c0
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetPreviousLocator, GetPreviousLocator method [Microsoft TV Technologies], GetPreviousLocator method [Microsoft TV Technologies],ITuneRequestInfo interface, ITuneRequestInfo interface [Microsoft TV Technologies],GetPreviousLocator method, ITuneRequestInfo.GetPreviousLocator, ITuneRequestInfo::GetPreviousLocator, ITuneRequestInfoGetPreviousLocator, bdatif/ITuneRequestInfo::GetPreviousLocator, mstv.itunerequestinfo_getpreviouslocator
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
 - ITuneRequestInfo.GetPreviousLocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITuneRequestInfo::GetPreviousLocator


## -description



The <b>GetPreviousLocator</b> method creates a new tune request with locator information for the previous transport stream.




## -parameters




### -param CurrentRequest

TBD


### -param TuneRequest

TBD




#### - pCurrentRequest [in]

Specifies current request.


#### - ppTuneRequest [out]

Pointer to a variable that receives the tune request for the previous transport stream in the network.


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



Currently this method is not implemented for DVB-C or DVB-S networks, and the method returns E_NOTIMPL. The method is implemented for DVB-T.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694998(v=VS.85).aspx">ITuneRequestInfo Interface</a>
 

 

