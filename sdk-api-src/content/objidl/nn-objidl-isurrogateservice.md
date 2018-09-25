---
UID: NN:objidl.ISurrogateService
title: ISurrogateService
author: windows-sdk-content
description: Used to initialize, launch, and release a COM+ application. You can also refresh the catalog and shut down the process.
old-location: com\isurrogateservice.htm
tech.root: com
ms.assetid: 01773aa6-3eb5-43dd-8a10-d1351a07fe1f
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ISurrogateService, ISurrogateService interface [COM], ISurrogateService interface [COM],described, _com_isurrogateservice, com.isurrogateservice, objidl/ISurrogateService
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - ObjIdl.h
api_name:
 - ISurrogateService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISurrogateService interface


## -description


<p class="CCE_Message">[Use of ISurrogateService is not recommended; use <a href="https://msdn.microsoft.com/acce67ef-3290-4892-b56a-77a256776c80">IProcessInitControl</a> instead.]

Used to initialize, launch, and release a COM+ application. You can also refresh the catalog and shut down the process.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISurrogateService</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>ISurrogateService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISurrogateService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/703de030-ac99-4673-8399-695116bf07d5">ApplicationFree</a>
</td>
<td align="left" width="63%">
Releases the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e54c129-f321-4215-b084-21ab17f93a6f">ApplicationLaunch</a>
</td>
<td align="left" width="63%">
Launches the application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e7b765b-0ba3-48db-afe2-2cb6257775fa">CatalogRefresh</a>
</td>
<td align="left" width="63%">
Refreshes the catalog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed2e628c-5c86-48fd-aa55-f532602247ea">Init</a>
</td>
<td align="left" width="63%">
Initializes the process server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b01dc079-647c-4e58-a36b-0a665355afb7">ProcessShutdown</a>
</td>
<td align="left" width="63%">
Shuts down the process.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/acce67ef-3290-4892-b56a-77a256776c80">IProcessInitControl</a>
 

 

