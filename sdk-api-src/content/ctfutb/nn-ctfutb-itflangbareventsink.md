---
UID: NN:ctfutb.ITfLangBarEventSink
title: ITfLangBarEventSink
author: windows-sdk-content
description: The ITfLangBarEventSink interface is implemented by an application or text service and used by the language bar to supply notifications of certain events that occur in the language bar.
old-location: tsf\itflangbareventsink.htm
old-project: TSF
ms.assetid: 2ef8b8ff-6549-41f8-baf3-3c5b8e2411a3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfLangBarEventSink, ITfLangBarEventSink interface [Text Services Framework], ITfLangBarEventSink interface [Text Services Framework],described, _tsf_itflangbareventsink_ref, ctfutb/ITfLangBarEventSink, tsf.itflangbareventsink
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TfLBIClick
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msutb.dll
api_name:
 - ITfLangBarEventSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Msutb.dll
req.irql: 
---

# ITfLangBarEventSink interface


## -description


The <b>ITfLangBarEventSink</b> interface is implemented by an application or text service and used by the language bar to supply notifications of certain events that occur in the language bar. The application or text service installs this event sink by calling <a href="https://msdn.microsoft.com/8ac607fd-b2c4-4441-8738-c64c25b6c586">ITfLangBarMgr::AdviseEventSink</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfLangBarEventSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfLangBarEventSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfLangBarEventSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05747d41-1342-4189-b654-ceb8fadcadd5">GetItemFloatingRect</a>
</td>
<td align="left" width="63%">
Not currently used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/781efe26-f3f4-401b-9558-d228e875abc4">OnModalInput</a>
</td>
<td align="left" width="63%">
Not currently used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66d70ff3-dcd4-42cd-bda4-7dbdf1c99da5">OnSetFocus</a>
</td>
<td align="left" width="63%">
Called when the thread the event sink was installed from receives the input focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b59688f9-feb0-4598-bf4a-b0661dda5fad">OnThreadItemChange</a>
</td>
<td align="left" width="63%">
Called when a language bar item changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cdb5d505-524b-4fbc-a90a-181d22cbadbc">OnThreadTerminate</a>
</td>
<td align="left" width="63%">
Not currently used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f667762a-f276-4311-827e-f89eca7eba1e">ShowFloating</a>
</td>
<td align="left" width="63%">
Called when ITfLangBarMgr::ShowFloating is called.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8ac607fd-b2c4-4441-8738-c64c25b6c586">ITfLangBarMgr::AdviseEventSink
      </a>



<a href="https://msdn.microsoft.com/f49987c7-476d-4add-9d43-83de78693420">ITfLangBarMgr::ShowFloating
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

