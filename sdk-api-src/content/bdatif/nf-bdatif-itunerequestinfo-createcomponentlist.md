---
UID: NF:bdatif.ITuneRequestInfo.CreateComponentList
title: ITuneRequestInfo::CreateComponentList
author: windows-sdk-content
description: The CreateComponentList method creates a new Components collection for the tune request, and fills it in with all network-specific data after the receiver has tuned to the service.
old-location: mstv\itunerequestinfo_createcomponentlist.htm
tech.root: MSTV
ms.assetid: cb4ec234-1e94-4c9f-8372-a5972df18948
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CreateComponentList, CreateComponentList method [Microsoft TV Technologies], CreateComponentList method [Microsoft TV Technologies],ITuneRequestInfo interface, ITuneRequestInfo interface [Microsoft TV Technologies],CreateComponentList method, ITuneRequestInfo.CreateComponentList, ITuneRequestInfo::CreateComponentList, ITuneRequestInfoCreateComponentList, bdatif/ITuneRequestInfo::CreateComponentList, mstv.itunerequestinfo_createcomponentlist
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
 - ITuneRequestInfo.CreateComponentList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITuneRequestInfo::CreateComponentList


## -description



The <b>CreateComponentList</b> method creates a new <a href="https://msdn.microsoft.com/6d779095-12f9-4e00-a25f-0a840f5149fa">Components</a> collection for the tune request, and fills it in with all network-specific data after the receiver has tuned to the service.




## -parameters




### -param CurrentRequest

TBD




#### - pCurrentRequest [in]

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
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
No data could be acquired.

</td>
</tr>
</table>
 




## -remarks



After the Network Provider has acquired the correct transport stream, it asks the TIF to fill in the component data. If the tune request does not already have a components list, the Network Provider calls this method and asks the TIF to create one based on the relevant transport stream tables. Generally, the components will include one or more audio streams, video, data, and text. Each component has a component type, and on MPEG2 tuning spaces each component has an associated PID and pcrPID. Ideally, when the Guide Store Loader creates tune requests, it will include all the component information that is available.

The <a href="https://msdn.microsoft.com/769d112e-4df7-451c-ac12-440b16c33e88">ITuneRequestInfo::GetComponentData</a> method is used to enable the TIF to change an existing list of components. S_FALSE indicates nothing was changed.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/e5cb1a15-29c4-4e0f-aed2-eafe12ea007a">ITuneRequestInfo Interface</a>
 

 

