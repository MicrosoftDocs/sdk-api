---
UID: NN:comsvcs.IServiceSxsConfig
title: IServiceSxsConfig (comsvcs.h)
description: Configures side-by-side assemblies for the work that is done when calling either CoCreateActivity or CoEnterServiceDomain.
old-location: cos\iservicesxsconfig.htm
tech.root: cossdk
ms.assetid: 24d4a22b-0a01-4bf2-9cc6-4a1b31897d05
ms.date: 12/05/2018
ms.keywords: IServiceSxSConfig, IServiceSxSConfig interface [COM+], IServiceSxSConfig interface [COM+],described, _cos_IServiceSxsConfig, comsvcs/IServiceSxSConfig, cos.iservicesxsconfig
ms.topic: interface
f1_keywords:
- comsvcs/IServiceSxSConfig
dev_langs:
- c++
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
- IServiceSxSConfig
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IServiceSxsConfig interface


## -description


Configures side-by-side assemblies for the work that is done when calling either <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a> or <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceSxSConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IServiceSxSConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServiceSxSConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicesxsconfig-sxsconfig">SxsConfig</a>
</td>
<td align="left" width="63%">
Configures the side-by-side assembly for the enclosed work.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicesxsconfig-sxsdirectory">SxsDirectory</a>
</td>
<td align="left" width="63%">
Sets the directory for the side-by-side assembly for the enclosed work.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicesxsconfig-sxsname">SxsName</a>
</td>
<td align="left" width="63%">
Sets the file name of the side-by-side assembly for the enclosed work.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal">Isolated Applications and Side-by-side Assemblies</a>
 

 

