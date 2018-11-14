---
UID: NN:ctfutb.ITfLangBarMgr
title: ITfLangBarMgr
author: windows-sdk-content
description: The ITfLangBarMgr interface is implemented by the TSF manager and used by text services to manage event sink notification and configure floating language bar display settings. The interface ID is IID_ITfLangBarMgr.
old-location: tsf\itflangbarmgr.htm
tech.root: TSF
ms.assetid: 60bd765f-0846-47f5-af1b-bc8e72720841
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ITfLangBarMgr, ITfLangBarMgr interface [Text Services Framework], ITfLangBarMgr interface [Text Services Framework],described, _tsf_itflangbarmgr_ref, ctfutb/ITfLangBarMgr, tsf.itflangbarmgr
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfLangBarMgr interface


## -description


The <b>ITfLangBarMgr</b> interface is implemented by the TSF manager and used by text services to manage event sink notification and configure floating language bar display settings. The interface ID is IID_ITfLangBarMgr.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfLangBarMgr</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfLangBarMgr</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8ac607fd-b2c4-4441-8738-c64c25b6c586">AdviseEventSink</a>
</td>
<td align="left" width="63%">
Advises a sink about a language bar event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/679d101b-b3f9-4771-9c68-729a6a3486de">GetInputProcessorProfiles</a>
</td>
<td align="left" width="63%">
Should not be used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec187bf0-edf7-4d90-a102-92bb5b58ebdc">GetShowFloatingStatus</a>
</td>
<td align="left" width="63%">
Obtains current language bar display settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ca37268-eb27-4d8b-9a16-306f77369e8f">GetThreadLangBarItemMgr</a>
</td>
<td align="left" width="63%">
Should not be used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9adfc307-ab22-4dfb-a5a8-40d9ad4900ad">GetThreadMarshalInterface</a>
</td>
<td align="left" width="63%">
Should not be used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/376e1f64-1a4f-4800-a049-7f2abb4ea605">RestoreLastFocus</a>
</td>
<td align="left" width="63%">
Should not be used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/754376e0-e7e4-4bd2-b89c-43d211634c65">SetModalInput</a>
</td>
<td align="left" width="63%">
Should not be used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f49987c7-476d-4add-9d43-83de78693420">ShowFloating</a>
</td>
<td align="left" width="63%">
Configures display settings for the floating language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29dc5276-04fa-4219-a64d-10d775d73fdd">UnadviseEventSink</a>
</td>
<td align="left" width="63%">
Uninstalls an advise event sink.

</td>
</tr>
</table> 


## -see-also




<a href="_com_cocreateinstance">CoCreateInstance</a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

