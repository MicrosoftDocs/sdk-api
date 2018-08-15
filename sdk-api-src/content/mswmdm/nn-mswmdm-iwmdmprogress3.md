---
UID: NN:mswmdm.IWMDMProgress3
title: IWMDMProgress3
author: windows-sdk-content
description: The optional, application-implemented IWMDMProgress3 interface extends IWMDMProgress2 by providing additional input parameters to specify which event is being monitored, and to allow for context-specific information.Applications that implement this callback interface should provide an implementation for methods corresponding to IWMDMProgress and IWMDMProgress2 for backward compatibility, in addition to the new methods.
old-location: wmdm\iwmdmprogress3.htm
old-project: WMDM
ms.assetid: fc3a7031-ac1b-45cf-889b-2d40d50b347d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMDMProgress3, IWMDMProgress3 interface [windows Media Device Manager], IWMDMProgress3 interface [windows Media Device Manager],described, IWMDMProgress3Interface, mswmdm/IWMDMProgress3, wmdm.iwmdmprogress3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mswmdm.h
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
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IWMDMProgress3
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMProgress3 interface


## -description



The optional, application-implemented <b>IWMDMProgress3</b> interface extends <b>IWMDMProgress2</b> by providing additional input parameters to specify which event is being monitored, and to allow for context-specific information.

Applications that implement this callback interface should provide an implementation for methods corresponding to <b>IWMDMProgress</b> and <b>IWMDMProgress2</b> for backward compatibility, in addition to the new methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMProgress3</b> interface inherits from <a href="https://msdn.microsoft.com/9af022a6-19b4-41b7-b951-0acad6aab4a2">IWMDMProgress</a>. <b>IWMDMProgress3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMProgress3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c794aff-9800-405e-853a-56dd5bd84665">Begin3</a>
</td>
<td align="left" width="63%">
Indicates that an operation is about to begin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb09cfa8-1a96-412f-a97a-6cc1638b0c77">End3</a>
</td>
<td align="left" width="63%">
Indicates that an operation is finished.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33f1de9c-f2eb-4b83-89a1-404a8c50ee08">Progress3</a>
</td>
<td align="left" width="63%">
Indicates the status of an action in progress.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b4fc7714-a7d0-409f-a47c-4903bab883cc">Enabling Notifications</a>



<a href="https://msdn.microsoft.com/9af022a6-19b4-41b7-b951-0acad6aab4a2">IWMDMProgress Interface</a>



<a href="https://msdn.microsoft.com/59619571-0ab7-42a4-ad25-c420ec9667a3">IWMDMProgress2 Interface</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

