---
UID: NN:mergemod.IMsmGetFiles
title: IMsmGetFiles
author: windows-sdk-content
description: The IMsmGetFiles interface enables the client to retrieve the files needed in a particular language of the module.
old-location: setup\imsmgetfiles_interface.htm
tech.root: msi
ms.assetid: d6912c92-b3e0-4b3d-a618-17e252cd14ae
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IMsmGetFiles, IMsmGetFiles interface, IMsmGetFiles interface,described, mergemod/IMsmGetFiles, setup.imsmgetfiles_interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
 - IMsmGetFiles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMsmGetFiles interface


## -description


The <b>IMsmGetFiles</b> interface enables the client to retrieve the files needed in a particular language of the
 module.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMsmGetFiles</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IMsmGetFiles</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMsmGetFiles</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/525c1a30-a870-4303-b704-e8b37f9e641f">get_ModuleFiles</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://msdn.microsoft.com/e1c8049c-b271-4def-abde-89ea99393574">ModuleFiles</a> property of the 
<a href="https://msdn.microsoft.com/f3bf64ec-75f7-43a6-bbd8-a51508c57002">GetFiles</a> object.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

