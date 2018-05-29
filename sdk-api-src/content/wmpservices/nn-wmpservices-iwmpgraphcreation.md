---
UID: NN:wmpservices.IWMPGraphCreation
title: IWMPGraphCreation
author: windows-sdk-content
description: The IWMPGraphCreation interface provides methods that Windows Media Player calls to enable you to manage the DirectShow filter graph.
old-location: wmp\iwmpgraphcreation.htm
old-project: WMP
ms.assetid: 80d6f1f0-10c9-4e60-9bb7-556e340730a8
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPGraphCreation, IWMPGraphCreation interface [Windows Media Player], IWMPGraphCreation interface [Windows Media Player],described, IWMPGraphCreationInterface, wmp.iwmpgraphcreation, wmpservices/IWMPGraphCreation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmpservices.h
req.include-header: 
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
req.typenames: WMPServices_StreamState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmpservices.h
api_name:
-	IWMPGraphCreation
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPGraphCreation interface


## -description





The <b>IWMPGraphCreation</b> interface provides methods that Windows Media Player calls to enable you to manage the DirectShow filter graph. It can be implemented by an application that embeds the Windows Media Player control.

The Windows Media Player control retrieves a pointer to this interface by calling <b>IServiceProvider::QueryService</b>. When you implement <b>IWMPGraphCreation</b>, you must also implement <b>IServiceProvider</b> and return the correct pointer when <b>QueryService</b> is called with IID_IWMPGraphCreation as the value for the second parameter.

This interface is not supported when remoting the Windows Media Player control.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPGraphCreation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPGraphCreation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPGraphCreation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26cac321-f32a-4569-87a8-f397173f058b">GetGraphCreationFlags</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player to retrieve a value that represents the graph creation preferences.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/243fc72e-ef97-49a6-9a50-05ec338e5faa">GraphCreationPostRender</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player after a file has been rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3375fa9-2ab0-4e82-9196-0b3971a00185">GraphCreationPreRender</a>
</td>
<td align="left" width="63%">
Called by Windows Media Player before a file has been rendered.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

