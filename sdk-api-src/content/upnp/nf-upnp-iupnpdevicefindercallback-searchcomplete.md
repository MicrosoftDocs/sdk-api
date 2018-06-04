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

# IUPnPDeviceFinderCallback::SearchComplete


## -description


The 
<b>SearchComplete</b> method is invoked by the UPnP framework to notify the application that the initial search for network devices has been completed.

This method is invoked when the UPnP framework has finished sending <a href="https://msdn.microsoft.com/4a61ca43-cbc6-4db2-9706-23cadbae9c3e">IUPnPDeviceFinderCallback::DeviceAdded</a> or <a href="https://msdn.microsoft.com/c7cd47e8-264b-4d1a-aed3-daf5801c240c">IUPnPDeviceFinderAddCallbackWithInterface::DeviceAddedWithInterface</a> callbacks for all devices that were present on the network at the time the search was started. These callbacks reflect the state of the network at the time the search was started.


## -parameters




### -param lFindData [in]

Specifies the search for which the UPnP framework is returning results. The value of <i>lFindData</i> is the value returned to the caller by 
<a href="https://msdn.microsoft.com/4461b53f-b630-4b4a-bc68-0cc48ef70594">IUPnPDeviceFinder::CreateAsyncFind</a>.


## -returns



The application should return S_OK.




## -remarks



This method simply provides information. It does not indicate that the asynchronous search has ended, but rather that the initial probe has completed. The asynchronous search continues to report devices being added to and removed from the network until the application calls 
<a href="https://msdn.microsoft.com/d64db4fe-0b0a-430f-b198-dd49ef40b52e">IUPnPDeviceFinder::CancelAsyncFind</a>.

The initial search can take a long time to complete. The <b>SearchComplete</b> callback is invoked when the description document for the last device found (that is, the last device found to be present on the network at the time the search was started) has either been loaded or has failed to load.




## -see-also




<a href="https://msdn.microsoft.com/a4697038-8abc-42f2-9381-702fc82af90b">IUPnPDeviceFinder</a>



<a href="https://msdn.microsoft.com/4461b53f-b630-4b4a-bc68-0cc48ef70594">IUPnPDeviceFinder::CreateAsyncFind</a>



<a href="https://msdn.microsoft.com/02f1220b-d400-469e-8a28-64871f7fcbe2">IUPnPDeviceFinderCallback</a>
 

 

