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

# IWMDRMReader::MonitorLicenseAcquisition


## -description


<p class="CCE_Message">[<b>MonitorLicenseAcquisition</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>MonitorLicenseAcquisition</b> method, in non-silent license acquisition, informs the application when a license has been successfully acquired.




## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method should be used whenever non-silent license acquisition has been initiated for DRM version 7 content. It is an asynchronous call that returns immediately. This method creates a thread that periodically checks the local license store to determine when the requested license has been received. To cancel the attempt, call <b>CancelMonitorLicenseAcquisition</b>.

When the license acquisition is completed (whether successful or otherwise), the application is notified through a <b>WMT_LICENSE_ACQUIRE</b> event that is sent to the application's <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> method.




## -see-also




<a href="https://msdn.microsoft.com/e118bf09-1fa6-41b6-a6bb-3e8cb6097994">Handling License Acquisition Events</a>



<a href="https://msdn.microsoft.com/bf4ff0f3-1f78-43c4-be4d-c74209176e58">IWMDRMReader Interface</a>



<a href="https://msdn.microsoft.com/9d33f727-9213-4744-bf65-42b971e3f7da">IWMDRMReader::CancelMonitorLicenseAcquisition</a>



<a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a>
 

 

