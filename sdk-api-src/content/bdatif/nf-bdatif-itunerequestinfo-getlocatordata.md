---
UID: NF:bdatif.ITuneRequestInfo.GetLocatorData
title: ITuneRequestInfo::GetLocatorData
author: windows-sdk-content
description: The GetLocatorData method fills in channel or program locator information for the specified tune request.
old-location: mstv\itunerequestinfo_getlocatordata.htm
old-project: mstv
ms.assetid: c325d61d-c99b-4033-bd16-36b74fc38d07
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetLocatorData, GetLocatorData method [Microsoft TV Technologies], GetLocatorData method [Microsoft TV Technologies],ITuneRequestInfo interface, ITuneRequestInfo interface [Microsoft TV Technologies],GetLocatorData method, ITuneRequestInfo.GetLocatorData, ITuneRequestInfo::GetLocatorData, ITuneRequestInfoGetLocatorData, bdatif/ITuneRequestInfo::GetLocatorData, mstv.itunerequestinfo_getlocatordata
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SmartCardApplication
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - ITuneRequestInfo.GetLocatorData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ITuneRequestInfo::GetLocatorData


## -description



The <b>GetLocatorData</b> method fills in channel or program locator information for the specified tune request.




## -parameters




### -param Request






#### - pRequest [in]

Pointer to the <a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a> interface on the tune request.


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
The method succeeded and new locator data was acquired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded but no new locator data was acquired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>Request</i> is not valid.

</td>
</tr>
</table>
 




## -remarks



After the TIF fills in the locator information, the Network Provider uses that information to configure the tuner and demodulator. It is expected that the TIF will always know everything about a locator. If it doesn't know how to locate a specific tune request, it can always fall back to the default locator for the tuning space. As soon as the TIF starts getting tables from the default stream, it signals the Network Provider, which then asks for the new locator data. When the TIF fills that in, it signals the Network Provider, which tunes again using the new information. When the TIF begins getting tables on the new stream, it signals the Network Provider again, and the process is repeated.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/e5cb1a15-29c4-4e0f-aed2-eafe12ea007a">ITuneRequestInfo Interface</a>
 

 

