---
UID: NN:comsvcs.IServiceSxsConfig
title: IServiceSxsConfig
author: windows-sdk-content
description: Configures side-by-side assemblies for the work that is done when calling either CoCreateActivity or CoEnterServiceDomain.
old-location: cos\iservicesxsconfig.htm
old-project: cossdk
ms.assetid: 24d4a22b-0a01-4bf2-9cc6-4a1b31897d05
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IServiceSxSConfig, IServiceSxSConfig interface [COM+], IServiceSxSConfig interface [COM+],described, _cos_IServiceSxsConfig, comsvcs/IServiceSxSConfig, cos.iservicesxsconfig
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IServiceSxSConfig
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServiceSxsConfig interface


## -description


Configures side-by-side assemblies for the work that is done when calling either <a href="https://msdn.microsoft.com/3009eb4f-e3f3-497b-ba05-5b750d8a40d0">CoCreateActivity</a> or <a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceSxSConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IServiceSxSConfig</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ce067aca-8bb4-48ac-b466-9080d2166bdd">SxsConfig</a>
</td>
<td align="left" width="63%">
Configures the side-by-side assembly for the enclosed work.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5eb909a5-7730-4f0b-aee6-9bb8de076cea">SxsDirectory</a>
</td>
<td align="left" width="63%">
Sets the directory for the side-by-side assembly for the enclosed work.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/622632ba-1287-4303-a9dd-4fb870e43786">SxsName</a>
</td>
<td align="left" width="63%">
Sets the file name of the side-by-side assembly for the enclosed work.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>



<a href="https://msdn.microsoft.com/2f841eb6-9a6c-4c9b-b057-a3da6cd6b0b0">Isolated Applications and Side-by-side Assemblies</a>
 

 

