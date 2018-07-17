---
UID: NN:msctf.ITfTextLayoutSink
title: ITfTextLayoutSink
author: windows-sdk-content
description: The ITfTextLayoutSink interface supports the context layout change by an application. Install this advise sink by calling ITfSource::AdviseSink with IID_ITfTextLayoutSink. A text service can optionally implement this interface.
old-location: tsf\itftextlayoutsink.htm
old-project: TSF
ms.assetid: 370e30a8-6eed-448a-87c7-7fd01e9973c6
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ITfTextLayoutSink, ITfTextLayoutSink interface [Text Services Framework], ITfTextLayoutSink interface [Text Services Framework],described, _tsf_itftextlayoutsink_ref, msctf/ITfTextLayoutSink, tsf.itftextlayoutsink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITfTextLayoutSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfTextLayoutSink interface


## -description


The <b>ITfTextLayoutSink</b> interface supports the context layout change by an application. Install this advise sink by calling <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a> with IID_ITfTextLayoutSink. A text service can optionally implement this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfTextLayoutSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfTextLayoutSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfTextLayoutSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a99313ab-98a7-4fc0-b3ae-78ff26a41d8e">OnLayoutChange</a>
</td>
<td align="left" width="63%">
Receives a notification when the layout of a context view changes.

</td>
</tr>
</table> 


## -remarks



TSF does not currently support multiple views; some features of this interface are limited.




## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">
        ITfContext
      </a>



<a href="https://msdn.microsoft.com/302d185d-dab7-4a77-a5cf-da2529d8b24a">ITfContextView
      </a>



<a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">
        ITfSource::AdviseSink
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

