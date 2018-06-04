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

# IQualProp::get_DevSyncOffset


## -description



The <code>get_DevSyncOffset</code> method retrieves the average time difference between when the video frames should have been displayed and when they actually were. This method is the same as the <a href="https://msdn.microsoft.com/4bed68f0-d080-46d4-b582-e561ddca33f0">IQualProp::get_AvgSyncOffset</a> method except that the value returned is calculated as a standard deviation rather than as a simple average.




## -parameters




### -param piDev

Pointer to a value denoting the accuracy of the video frames displayed.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



When playing video from networks, the presentation can often be disrupted by network glitches. For this reason, expressing the accuracy of video frames by a simple average is inappropriate. Looking at a standard deviation provides a better idea of the overall accuracy.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/428dfb97-0dfa-442c-819e-291e6a58f712">IQualProp Interface</a>
 

 

