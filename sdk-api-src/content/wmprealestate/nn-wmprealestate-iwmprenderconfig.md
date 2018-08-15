---
UID: NN:wmprealestate.IWMPRenderConfig
title: IWMPRenderConfig
author: windows-sdk-content
description: The IWMPRenderConfig interface provides methods to specify or retrieve a value indicating whether Media Foundation&#8211;based playback is restricted to the current process.Note  Using this interface with protected content is not supported. .
old-location: wmp\iwmprenderconfig.htm
old-project: WMP
ms.assetid: 01a4c79e-9867-47c0-9aca-b2f1596f1c2a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPRenderConfig, IWMPRenderConfig interface [Windows Media Player], IWMPRenderConfig interface [Windows Media Player],described, IWMPRenderConfigInterface, wmp.iwmprenderconfig, wmprealestate/IWMPRenderConfig
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmprealestate.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
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
tech.root: 
req.typenames: WMP_WMDM_METADATA_ROUND_TRIP_PC2DEVICE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmprealestate.h
api_name:
 - IWMPRenderConfig
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPRenderConfig interface


## -description



The <b>IWMPRenderConfig</b> interface provides methods to specify or retrieve a value indicating whether Media Foundation–based playback is restricted to the current process.

<div class="alert"><b>Note</b>  Using this interface with protected content is not supported.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPRenderConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPRenderConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPRenderConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71284af6-dc76-4a39-81f4-ed265140aad5">get_inProcOnly</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether playback is restricted to the current process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd7c7cbc-f428-46e1-b239-74b78cbf5835">put_inProcOnly</a>
</td>
<td align="left" width="63%">
Specifies a value indicating whether playback is restricted to the current process.

</td>
</tr>
</table> 

Retrieve a pointer to <b>IWMPRenderConfig</b> by calling <b>QueryInterface</b> through a pointer to <a href="https://msdn.microsoft.com/ce6aef79-1faa-44ac-a096-f65d09458067">IWMPPlayer</a>.

	


## -see-also




<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

