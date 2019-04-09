---
UID: NF:bdatif.ITuneRequestInfo.GetComponentData
title: ITuneRequestInfo::GetComponentData (bdatif.h)
author: windows-sdk-content
description: The GetComponentData method fills in all network-specific component data for the existing Components collection on the specified tune request.
old-location: mstv\itunerequestinfo_getcomponentdata.htm
tech.root: mstv
ms.assetid: 769d112e-4df7-451c-ac12-440b16c33e88
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetComponentData, GetComponentData method [Microsoft TV Technologies], GetComponentData method [Microsoft TV Technologies],ITuneRequestInfo interface, ITuneRequestInfo interface [Microsoft TV Technologies],GetComponentData method, ITuneRequestInfo.GetComponentData, ITuneRequestInfo::GetComponentData, ITuneRequestInfoGetComponentData, bdatif/ITuneRequestInfo::GetComponentData, mstv.itunerequestinfo_getcomponentdata
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
 - ITuneRequestInfo.GetComponentData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITuneRequestInfo::GetComponentData


## -description



The <b>GetComponentData</b> method fills in all network-specific component data for the existing <a href="https://msdn.microsoft.com/6d779095-12f9-4e00-a25f-0a840f5149fa">Components</a> collection on the specified tune request.




## -parameters




### -param CurrentRequest [in]

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
The method succeeded and new data was added.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded but no new data was added.

</td>
</tr>
</table>
 




## -remarks



The Network Provider calls this method after the tuner has tuned to the specified service.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/e5cb1a15-29c4-4e0f-aed2-eafe12ea007a">ITuneRequestInfo Interface</a>
 

 

