---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IGraphConfig::Reconfigure


## -description



The <code>Reconfigure</code> method locks the filter graph and calls a callback function in the application or filter to perform a dynamic reconfiguration.




## -parameters




### -param pCallback [in]

Pointer to the <a href="https://msdn.microsoft.com/b7856181-1616-4984-bf5e-402140ab7b4e">IGraphConfigCallback</a> callback interface on the application or filter.


### -param pvContext [in]

Pointer to a variable of type <b>PVOID</b> that is passed to the callback routine.


### -param dwFlags [in]

Application-defined flags that are passed to the callback routine.


### -param hAbortEvent [in]

Handle to an event. If the caller is a filter calling on one of its data processing threads, this parameter should be a handle to an event that will be signaled when the filter is put into a stopped state. Otherwise, this parameter can be <b>NULL</b>. For more information, see Remarks.


## -returns



Returns S_OK if successful, or an error code otherwise. Possible errors include VFW_E_WRONG_STATE, if the method could not obtain a lock on the filter graph; whatever <b>HRESULT</b> was returned by the callback routine; or an error code indicating that the graph could not put the filters into a running state.




## -remarks



This method is provided so that an application or filter can implement specialized dynamic graph building. In most cases, however, the <a href="https://msdn.microsoft.com/e8cfac8e-df89-444d-bcc7-0cbc7ab5a592">IGraphConfig::Reconnect</a> method is adequate, and should be preferred because it handles most of the implementation details.

Before calling this method, block any streams as needed and push the data through the graph (see <a href="https://msdn.microsoft.com/9bcd325d-41fc-4166-8fce-50fc921efdba">IPinFlowControl::Block</a> and <a href="https://msdn.microsoft.com/f3d72a32-f43a-4a61-b25e-6d472aa629de">IGraphConfig::PushThroughData</a>). If the callback method succeeds, <code>IGraphConfig::Reconfigure</code> attempts to put all the filters into a running state. (The caller must then unblock the data flow.) Otherwise, it returns whatever error code the callback method returned.

If a filter calls this method on one of its own data processing threads, it creates the potential for a deadlock. The method obtains a lock on the filter graph, which can block the filter from stopping on receiving a call to <a href="https://msdn.microsoft.com/8c415b5c-1aee-4ea4-b182-fd95da4898aa">IMediaFilter::Stop</a>. To prevent this situation, the method takes a handle to an event object provided by filter. The filter should signal the event if it receives a call to its <b>Stop</b> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7df22157-9dd1-410e-b037-a155f7b9a01b">IGraphConfig Interface</a>
 

 

