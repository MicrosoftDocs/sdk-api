---
UID: NN:ctfutb.ITfLangBarMgr
title: ITfLangBarMgr (ctfutb.h)
description: The ITfLangBarMgr interface is implemented by the TSF manager and used by text services to manage event sink notification and configure floating language bar display settings. The interface ID is IID_ITfLangBarMgr.
old-location: tsf\itflangbarmgr.htm
tech.root: TSF
ms.assetid: 60bd765f-0846-47f5-af1b-bc8e72720841
ms.date: 12/05/2018
ms.keywords: ITfLangBarMgr, ITfLangBarMgr interface [Text Services Framework], ITfLangBarMgr interface [Text Services Framework],described, _tsf_itflangbarmgr_ref, ctfutb/ITfLangBarMgr, tsf.itflangbarmgr
ms.topic: interface
f1_keywords:
- ctfutb/ITfLangBarMgr
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
req.dll: Msctf.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- msctf.dll
api_name:
- ITfLangBarMgr
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfLangBarMgr interface


## -description


The <b>ITfLangBarMgr</b> interface is implemented by the TSF manager and used by text services to manage event sink notification and configure floating language bar display settings. The interface ID is IID_ITfLangBarMgr.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfLangBarMgr</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfLangBarMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfLangBarMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-adviseeventsink">AdviseEventSink</a>
</td>
<td align="left" width="63%">
Advises a sink about a language bar event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-getinputprocessorprofiles">GetInputProcessorProfiles</a>
</td>
<td align="left" width="63%">
Should not be used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-getshowfloatingstatus">GetShowFloatingStatus</a>
</td>
<td align="left" width="63%">
Obtains current language bar display settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-getthreadlangbaritemmgr">GetThreadLangBarItemMgr</a>
</td>
<td align="left" width="63%">
Should not be used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-getthreadmarshalinterface">GetThreadMarshalInterface</a>
</td>
<td align="left" width="63%">
Should not be used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-restorelastfocus">RestoreLastFocus</a>
</td>
<td align="left" width="63%">
Should not be used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-setmodalinput">SetModalInput</a>
</td>
<td align="left" width="63%">
Should not be used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-showfloating">ShowFloating</a>
</td>
<td align="left" width="63%">
Configures display settings for the floating language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-unadviseeventsink">UnadviseEventSink</a>
</td>
<td align="left" width="63%">
Uninstalls an advise event sink.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

