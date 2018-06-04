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

# IMSVidInputDevice::View


## -description


The <b>View</b> method configures this input device to view the specified tune request.


## -parameters




### -param v






#### - pv [in]

Specifies the tune request as a <b>VARIANT</b> type.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Before calling this method, set the device as the active input by calling the <a href="https://msdn.microsoft.com/696d8ece-a377-4fe8-a790-a68d1a24e65a">IMSVidCtl::put_InputActive</a> method. Unless the application needs to choose a specific input device, however, the <a href="https://msdn.microsoft.com/ec0e2a88-13c0-42f3-ba7d-8ebff1234b86">IMSVidCtl::View</a> method is recommended instead of the <b>IMSVidInputDevice::View</b> method.




## -see-also




<a href="https://msdn.microsoft.com/5b413ade-4ab2-45fa-98b2-fd93c8f89a43">IMSVidInputDevice Interface</a>
 

 

