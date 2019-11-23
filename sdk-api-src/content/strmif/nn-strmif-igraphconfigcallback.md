---
UID: NN:strmif.IGraphConfigCallback
title: IGraphConfigCallback (strmif.h)

description: The IGraphConfigCallback interface contains the callback method passed to IGraphConfig::Reconfigure. The caller (an application or filter) implements this interface. For more information, see IGraphConfig.
old-location: dshow\igraphconfigcallback.htm
tech.root: DirectShow
ms.assetid: b7856181-1616-4984-bf5e-402140ab7b4e

ms.date: 12/05/2018
ms.keywords: IGraphConfigCallback, IGraphConfigCallback interface [DirectShow], IGraphConfigCallback interface [DirectShow],described, IGraphConfigCallbackInterface, dshow.igraphconfigcallback, strmif/IGraphConfigCallback
ms.topic: interface
f1_keywords: 
 - "strmif/IGraphConfigCallback"
dev_langs:
 - c++
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IGraphConfigCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGraphConfigCallback interface


## -description



The <code>IGraphConfigCallback</code> interface contains the callback method passed to <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphconfig-reconfigure">IGraphConfig::Reconfigure</a>. The caller (an application or filter) implements this interface. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-igraphconfig">IGraphConfig</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGraphConfigCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGraphConfigCallback</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphconfigcallback-reconfigure">Reconfigure</a>
</td>
<td align="left" width="63%">
Callback method passed to <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-igraphconfig-reconfigure">IGraphConfig::Reconfigure</a>.

</td>
</tr>
</table> 

