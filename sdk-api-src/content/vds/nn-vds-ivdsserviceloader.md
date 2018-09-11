---
UID: NN:vds.IVdsServiceLoader
title: IVdsServiceLoader
author: windows-sdk-content
description: Instantiates a service loader object.
old-location: base\ivdsserviceloader.htm
tech.root: VDS
ms.assetid: 43533ee7-4e44-48c9-8c9d-0992426d79ba
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IVdsServiceLoader, IVdsServiceLoader interface [VDS], IVdsServiceLoader interface [VDS],described, base.ivdsserviceloader, vds/IVdsServiceLoader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsServiceLoader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsServiceLoader interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Instantiates a service loader object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsServiceLoader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsServiceLoader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsServiceLoader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26bb0a1f-37ad-4bb0-af6c-1063c5ccdc0f">LoadService</a>
</td>
<td align="left" width="63%">
Launches VDS on the specified computer and returns a pointer to the service object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

