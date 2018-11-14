---
UID: NN:comsvcs.IServiceSxsConfig
title: IServiceSxsConfig
author: windows-sdk-content
description: Configures side-by-side assemblies for the work that is done when calling either CoCreateActivity or CoEnterServiceDomain.
old-location: cos\iservicesxsconfig.htm
tech.root: cossdk
ms.assetid: 24d4a22b-0a01-4bf2-9cc6-4a1b31897d05
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IServiceSxSConfig, IServiceSxSConfig interface [COM+], IServiceSxSConfig interface [COM+],described, _cos_IServiceSxsConfig, comsvcs/IServiceSxSConfig, cos.iservicesxsconfig
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IServiceSxSConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IServiceSxsConfig interface


## -description


Configures side-by-side assemblies for the work that is done when calling either <a href="https://msdn.microsoft.com/en-us/library/ms679553(v=VS.85).aspx">CoCreateActivity</a> or <a href="https://msdn.microsoft.com/en-us/library/ms683559(v=VS.85).aspx">CoEnterServiceDomain</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceSxSConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IServiceSxSConfig</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms686504(v=VS.85).aspx">SxsConfig</a>
</td>
<td align="left" width="63%">
Configures the side-by-side assembly for the enclosed work.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681742(v=VS.85).aspx">SxsDirectory</a>
</td>
<td align="left" width="63%">
Sets the directory for the side-by-side assembly for the enclosed work.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681787(v=VS.85).aspx">SxsName</a>
</td>
<td align="left" width="63%">
Sets the file name of the side-by-side assembly for the enclosed work.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd408052(v=VS.85).aspx">Isolated Applications and Side-by-side Assemblies</a>
 

 

