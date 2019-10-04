---
UID: NN:comsvcs.ICheckSxsConfig
title: ICheckSxsConfig (comsvcs.h)
author: windows-sdk-content
description: Used to check the configuration of the current side-by-side assembly.
old-location: cos\ichecksxsconfig.htm
tech.root: cossdk
ms.assetid: 34c97d61-694e-4ee3-92ed-55b0a787b747
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICheckSxSConfig, ICheckSxSConfig interface [COM+], ICheckSxSConfig interface [COM+],described, _cos_ICheckSxsConfig, comsvcs/ICheckSxSConfig, cos.ichecksxsconfig
ms.topic: interface
f1_keywords: 
 - "comsvcs/ICheckSxSConfig"
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
 - ICheckSxSConfig
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICheckSxsConfig interface


## -description


Used to check the configuration of the current side-by-side assembly.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICheckSxSConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICheckSxSConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICheckSxSConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-ichecksxsconfig-issamesxsconfig">IsSameSxsConfig</a>
</td>
<td align="left" width="63%">
Determines whether the side-by-side assembly has the specified configuration.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iservicesxsconfig">IServiceSxSConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal">Isolated Applications and Side-by-side Assemblies</a>
 

 

