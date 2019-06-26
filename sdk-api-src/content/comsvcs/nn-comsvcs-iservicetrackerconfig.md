---
UID: NN:comsvcs.IServiceTrackerConfig
title: IServiceTrackerConfig (comsvcs.h)
author: windows-sdk-content
description: Configures the tracker property for the work that is done when calling either CoCreateActivity or CoEnterServiceDomain.
old-location: cos\iservicetrackerconfig.htm
tech.root: cossdk
ms.assetid: 342713d0-be5e-4d47-85ba-b18673a17fb5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IServiceTrackerConfig, IServiceTrackerConfig interface [COM+], IServiceTrackerConfig interface [COM+],described, _cos_IServiceTrackerConfig, comsvcs/IServiceTrackerConfig, cos.iservicetrackerconfig
ms.topic: interface
f1_keywords: 
 - "comsvcs/IServiceTrackerConfig"
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
ms.custom: 19H1
---

# IServiceTrackerConfig interface


## -description


Configures the tracker property for the work that is done when calling either <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a> or <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceTrackerConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IServiceTrackerConfig</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicetrackerconfig-trackerconfig">TrackerConfig</a>
</td>
<td align="left" width="63%">
Configures the tracker property for the enclosed work.


</td>
</tr>
</table> 


## -remarks



The tracker property is a reporting mechanism used by monitoring code to watch which code is running when. It is the reporting mechanism behind the spinning balls in the Component Services administrative tool.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>
 

 

