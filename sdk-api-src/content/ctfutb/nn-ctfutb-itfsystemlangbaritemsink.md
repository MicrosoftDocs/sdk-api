---
UID: NN:ctfutb.ITfSystemLangBarItemSink
title: ITfSystemLangBarItemSink
author: windows-driver-content
description: The ITfSystemLangBarItemSink interface is implemented by a system language bar menu extension and used by a system language bar menu (host) to allow menu items to be added to an existing system language bar menu.
old-location: tsf\itfsystemlangbaritemsink.htm
old-project: TSF
ms.assetid: a88b20ec-fc54-4814-9ca1-131664b4f377
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfSystemLangBarItemSink, ITfSystemLangBarItemSink interface [Text Services Framework], ITfSystemLangBarItemSink interface [Text Services Framework],described, _tsf_itfsystemlangbaritemsink_ref, ctfutb/ITfSystemLangBarItemSink, tsf.itfsystemlangbaritemsink
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
-	ITfSystemLangBarItemSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfSystemLangBarItemSink interface


## -description


The <b>ITfSystemLangBarItemSink</b> interface is implemented by a system language bar menu extension and used by a system language bar menu (host) to allow menu items to be added to an existing system language bar menu. The extension obtains an instance of this interface by calling QueryInterface on the <a href="https://msdn.microsoft.com/16612641-2bff-4e6f-a955-85793021a20b">ITfLangBarItem</a> object with IID_ITfSystemLangBarItemSink. It can then pass the object to the host by calling <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfSystemLangBarItemSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfSystemLangBarItemSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfSystemLangBarItemSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e8ba0ef-2f0a-4d67-95c1-06fee763bc14">InitMenu</a>
</td>
<td align="left" width="63%">
Called to allow a system language bar item extension to add items to a system language bar menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43c20f95-64b5-458a-8469-0d8b284b66dd">OnMenuSelect</a>
</td>
<td align="left" width="63%">
Called when the user selects an item in the system menu added by the system language bar menu extension.

</td>
</tr>
</table> 


## -remarks



A system language bar menu is an object on the language bar that supports menu items added to it by third-partyextensions. The system item must support the <a href="https://msdn.microsoft.com/2ff77f09-1b4c-4115-9bb4-4040097d1f90">ITfSource</a> interface and support the IID_ITfSystemLangBarItemSink identifier in its <b>ITfSource::AdviseSink</b> implementation. The system item should also implement the <a href="https://msdn.microsoft.com/9b41e787-eb90-4858-8838-8c36c7dce0c1">ITfSystemLangBarItem</a> interface. The system item uses the <b>ITfSystemLangBarItemSink</b> interface to allow the extension to add its items.




## -see-also




<a href="https://msdn.microsoft.com/16612641-2bff-4e6f-a955-85793021a20b">
        ITfLangBarItem
      </a>



<a href="https://msdn.microsoft.com/2ff77f09-1b4c-4115-9bb4-4040097d1f90">ITfSource</a>



<a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a>



<a href="https://msdn.microsoft.com/9b41e787-eb90-4858-8838-8c36c7dce0c1">ITfSystemLangBarItem
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

