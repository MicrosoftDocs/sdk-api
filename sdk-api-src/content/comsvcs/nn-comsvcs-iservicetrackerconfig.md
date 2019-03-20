---
UID: NN:comsvcs.IServiceTrackerConfig
title: IServiceTrackerConfig (comsvcs.h)
author: windows-sdk-content
description: Configures the tracker property for the work that is done when calling either CoCreateActivity or CoEnterServiceDomain.
old-location: cos\iservicetrackerconfig.htm
tech.root: cossdk
ms.assetid: 342713d0-be5e-4d47-85ba-b18673a17fb5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IServiceTrackerConfig, IServiceTrackerConfig interface [COM+], IServiceTrackerConfig interface [COM+],described, _cos_IServiceTrackerConfig, comsvcs/IServiceTrackerConfig, cos.iservicetrackerconfig
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ComSvcs.h
api_name:
 - IServiceTrackerConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IServiceTrackerConfig interface


## -description


Configures the tracker property for the work that is done when calling either <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a> or <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceTrackerConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IServiceTrackerConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServiceTrackerConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cdeb982b-720a-4d69-9c3c-d7a5a4527991">TrackerConfig</a>
</td>
<td align="left" width="63%">
Configures the tracker property for the enclosed work.


</td>
</tr>
</table> 


## -remarks



The tracker property is a reporting mechanism used by monitoring code to watch which code is running when. It is the reporting mechanism behind the spinning balls in the Component Services administrative tool.





## -see-also




<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>
 

 

