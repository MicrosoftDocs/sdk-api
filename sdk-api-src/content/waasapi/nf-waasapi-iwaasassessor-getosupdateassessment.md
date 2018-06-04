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

# IWaaSAssessor::GetOSUpdateAssessment


## -description


Gets the OS update assessment by comparing the latest release OS version from Microsoft to the OS build running on the device. 



## -parameters




### -param result [out, retval]

On success, contains a pointer to the OS update assessment.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 




## -remarks



<b>GetOSUpdateAssessment</b> retrieves the OS update assessment. The assessment provides information on updates applicable to a device: specifically, if the OS on the device is up-to-date. If the OS is not up-to-date, the assessment provides some reasons why. The assessment also suggests the potential impact being out-of-date has on the device.




## -see-also




<a href="https://msdn.microsoft.com/CE5D99C9-2348-4566-AC94-DFBA5B583503">IWaaSAssessor</a>
 

 

