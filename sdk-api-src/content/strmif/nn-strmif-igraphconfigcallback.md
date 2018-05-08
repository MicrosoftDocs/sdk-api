---
UID: NN:strmif.IGraphConfigCallback
title: IGraphConfigCallback
author: windows-driver-content
description: The IGraphConfigCallback interface contains the callback method passed to IGraphConfig::Reconfigure. The caller (an application or filter) implements this interface. For more information, see IGraphConfig.
old-location: dshow\igraphconfigcallback.htm
old-project: DirectShow
ms.assetid: b7856181-1616-4984-bf5e-402140ab7b4e
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IGraphConfigCallback, IGraphConfigCallback interface [DirectShow], IGraphConfigCallback interface [DirectShow],described, IGraphConfigCallbackInterface, dshow.igraphconfigcallback, strmif/IGraphConfigCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IGraphConfigCallback
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IGraphConfigCallback interface


## -description



The <code>IGraphConfigCallback</code> interface contains the callback method passed to <a href="https://msdn.microsoft.com/924087c0-e3ad-437b-96e5-de39bbce2ea7">IGraphConfig::Reconfigure</a>. The caller (an application or filter) implements this interface. For more information, see <a href="https://msdn.microsoft.com/7df22157-9dd1-410e-b037-a155f7b9a01b">IGraphConfig</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGraphConfigCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGraphConfigCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGraphConfigCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4f44639-b3b0-412e-8b71-e1f994dee0e6">Reconfigure</a>
</td>
<td align="left" width="63%">
Callback method passed to <a href="https://msdn.microsoft.com/924087c0-e3ad-437b-96e5-de39bbce2ea7">IGraphConfig::Reconfigure</a>.

</td>
</tr>
</table> 

