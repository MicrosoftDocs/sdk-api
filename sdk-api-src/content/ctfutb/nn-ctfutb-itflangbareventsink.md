---
UID: NN:ctfutb.ITfLangBarEventSink
title: ITfLangBarEventSink (ctfutb.h)

description: The ITfLangBarEventSink interface is implemented by an application or text service and used by the language bar to supply notifications of certain events that occur in the language bar.
old-location: tsf\itflangbareventsink.htm
tech.root: TSF
ms.assetid: 2ef8b8ff-6549-41f8-baf3-3c5b8e2411a3

ms.date: 12/05/2018
ms.keywords: ITfLangBarEventSink, ITfLangBarEventSink interface [Text Services Framework], ITfLangBarEventSink interface [Text Services Framework],described, _tsf_itflangbareventsink_ref, ctfutb/ITfLangBarEventSink, tsf.itflangbareventsink
ms.topic: interface
f1_keywords: 
 - "ctfutb/ITfLangBarEventSink"
dev_langs:
 - c++
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
req.lib: 
req.dll: Msutb.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msutb.dll
api_name:
 - ITfLangBarEventSink
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfLangBarEventSink interface


## -description


The <b>ITfLangBarEventSink</b> interface is implemented by an application or text service and used by the language bar to supply notifications of certain events that occur in the language bar. The application or text service installs this event sink by calling <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-adviseeventsink">ITfLangBarMgr::AdviseEventSink</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfLangBarEventSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfLangBarEventSink</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbareventsink-getitemfloatingrect">GetItemFloatingRect</a>
</td>
<td align="left" width="63%">
Not currently used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbareventsink-onmodalinput">OnModalInput</a>
</td>
<td align="left" width="63%">
Not currently used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbareventsink-onsetfocus">OnSetFocus</a>
</td>
<td align="left" width="63%">
Called when the thread the event sink was installed from receives the input focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbareventsink-onthreaditemchange">OnThreadItemChange</a>
</td>
<td align="left" width="63%">
Called when a language bar item changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbareventsink-onthreadterminate">OnThreadTerminate</a>
</td>
<td align="left" width="63%">
Not currently used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbareventsink-showfloating">ShowFloating</a>
</td>
<td align="left" width="63%">
Called when ITfLangBarMgr::ShowFloating is called.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-adviseeventsink">ITfLangBarMgr::AdviseEventSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-showfloating">ITfLangBarMgr::ShowFloating
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

