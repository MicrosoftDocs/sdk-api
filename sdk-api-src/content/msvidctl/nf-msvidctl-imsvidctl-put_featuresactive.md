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

# IMSVidCtl::put_FeaturesActive


## -description


The <b>put_FeaturesActive</b> method specifies a collection of features to activate.


## -parameters




### -param pVal [in]

Pointer to the <a href="https://msdn.microsoft.com/19790fab-0530-4a17-8a3c-a50576fea9ca">IMSVidFeatures</a> interface on a collection of features.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



Features represent additional capabilities beyond basic tuning and rendering, such as closed captioning or IP data services. When the Video Control builds the filter graph, it uses the active features collection to configure the graph.

For a default graph, it is not necessary to specify the active features. To activate a feature, create a new <a href="https://msdn.microsoft.com/dd826afd-b6a1-449e-937b-8341506d3e1a">MSVidFeatures</a> collection object. Then use the <a href="https://msdn.microsoft.com/73da686c-0c25-4dfb-8a13-681f1dac6a4a">IMSVidCtl::get_FeaturesAvailable</a> method to enumerate the available features, and call <a href="https://msdn.microsoft.com/80890372-2d92-4a3a-963f-2a6ca6632c52">IMSVidDevice::get__ClassID</a> on each feature. If the CLSID matches the feature you wish to activate, add that feature to your MSVidFeatures collection. Then call <b>put_FeaturesActive</b> with a pointer to the MSVidFeatures collection.

If the Video Control's state is not <b>STATE_UNBUILT</b>, call the <a href="https://msdn.microsoft.com/e67bf380-dc2c-42c9-a995-17951c65fbda">IMSVidCtl::Decompose</a> to tear down the filter graph before calling this method.




## -see-also




<a href="https://msdn.microsoft.com/e3ea10ea-bfb4-4c35-9933-5ad0367fd9ee">IMSVidCtl Interface</a>



<a href="https://msdn.microsoft.com/33832fe2-e8ef-4e37-9af9-90f566feb559">IMSVidCtl::get_FeaturesActive</a>



<a href="https://msdn.microsoft.com/45f35832-709c-4f78-9e1a-a6ad489fc81f">IMSVidCtl::get_State</a>
 

 

