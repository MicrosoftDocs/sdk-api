---
UID: NN:mergemod.IMsmConfigureModule
title: IMsmConfigureModule
author: windows-sdk-content
description: The IMsmConfigureModule interface is a callback interface; it enables the client to provide merge configuration information during the merge process.
old-location: setup\imsmconfiguremodule_interface.htm
tech.root: msi
ms.assetid: 90e09449-6211-4eae-8fd1-446e0187ed6c
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: IMsmConfigureModule, IMsmConfigureModule interface, IMsmConfigureModule interface,described, mergemod/IMsmConfigureModule, setup.imsmconfiguremodule_interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 2.0 or later
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
req.lib: 
req.dll: Mergemod.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmConfigureModule
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMsmConfigureModule interface


## -description


The <b>IMsmConfigureModule</b> interface is a callback interface; it enables the client to provide merge configuration information during the
merge process.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMsmConfigureModule</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IMsmConfigureModule</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMsmConfigureModule</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d03ce35-2ded-4f65-a73f-2546d67b0454">ProvideIntegerData</a>
</td>
<td align="left" width="63%">
Retrieves integer data from the client tool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81803b47-e1b1-45b7-b59d-aac555b189f7">ProvideTextData</a>
</td>
<td align="left" width="63%">
Retrieves text data from the client tool.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

