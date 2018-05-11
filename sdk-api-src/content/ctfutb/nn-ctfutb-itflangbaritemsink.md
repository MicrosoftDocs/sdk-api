---
UID: NN:ctfutb.ITfLangBarItemSink
title: ITfLangBarItemSink
author: windows-driver-content
description: The ITfLangBarItemSink interface is implemented by the language bar and used by a language bar item provider to notify the language bar of changes to a language bar item.
old-location: tsf\itflangbaritemsink.htm
old-project: TSF
ms.assetid: 1734a011-1ee8-4afd-ace8-334eeaf14518
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITfLangBarItemSink, ITfLangBarItemSink interface [Text Services Framework], ITfLangBarItemSink interface [Text Services Framework],described, _tsf_itflangbaritemsink_ref, ctfutb/ITfLangBarItemSink, tsf.itflangbaritemsink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TfLBIClick
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfLangBarItemSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfLangBarItemSink interface


## -description


The <b>ITfLangBarItemSink</b> interface is implemented by the language bar and used by a language bar item provider to notify the language bar of changes to a language bar item.

The language bar item provider obtains an instance of this interface when the language bar calls the provider's <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a> with identifier IID_ITfLangBarItemSink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfLangBarItemSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfLangBarItemSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfLangBarItemSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926909">OnUpdate</a>
</td>
<td align="left" width="63%">
Notifies the language bar of a change in a language bar item.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

