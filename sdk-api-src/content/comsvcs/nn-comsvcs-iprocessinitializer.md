---
UID: NN:comsvcs.IProcessInitializer
title: IProcessInitializer
author: windows-sdk-content
description: Provides methods that can be called whenever Dllhost.exe starts up or shuts down.
old-location: cos\iprocessinitializer.htm
old-project: cossdk
ms.assetid: 7c7edeb7-5bc1-4ede-8fe4-78fc7c6bdd30
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IProcessInitializer, IProcessInitializer interface [COM+], IProcessInitializer interface [COM+],described, _cos_IProcessInitializer, comsvcs/IProcessInitializer, cos.iprocessinitializer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IProcessInitializer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IProcessInitializer interface


## -description


Provides methods that can be called whenever Dllhost.exe starts up or shuts down.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProcessInitializer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IProcessInitializer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProcessInitializer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a>
</td>
<td align="left" width="63%">
Called when Dllhost.exe shuts down.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ba8844e-a1ef-4a1a-aef6-abd828ec59b0">Startup</a>
</td>
<td align="left" width="63%">
Called when Dllhost.exe starts.


</td>
</tr>
</table> 

