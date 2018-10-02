---
UID: NN:ctfutb.ITfSystemLangBarItemSink
title: ITfSystemLangBarItemSink
author: windows-sdk-content
description: The ITfSystemLangBarItemSink interface is implemented by a system language bar menu extension and used by a system language bar menu (host) to allow menu items to be added to an existing system language bar menu.
old-location: tsf\itfsystemlangbaritemsink.htm
tech.root: TSF
ms.assetid: a88b20ec-fc54-4814-9ca1-131664b4f377
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITfSystemLangBarItemSink, ITfSystemLangBarItemSink interface [Text Services Framework], ITfSystemLangBarItemSink interface [Text Services Framework],described, _tsf_itfsystemlangbaritemsink_ref, ctfutb/ITfSystemLangBarItemSink, tsf.itfsystemlangbaritemsink
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
 - ITfSystemLangBarItemSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfSystemLangBarItemSink interface


## -description


The <b>ITfSystemLangBarItemSink</b> interface is implemented by a system language bar menu extension and used by a system language bar menu (host) to allow menu items to be added to an existing system language bar menu. The extension obtains an instance of this interface by calling QueryInterface on the <a href="https://msdn.microsoft.com/en-us/library/ms628701(v=VS.85).aspx">ITfLangBarItem</a> object with IID_ITfSystemLangBarItemSink. It can then pass the object to the host by calling <a href="https://msdn.microsoft.com/en-us/library/ms628945(v=VS.85).aspx">ITfSource::AdviseSink</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfSystemLangBarItemSink</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ITfSystemLangBarItemSink</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms628958(v=VS.85).aspx">InitMenu</a>
</td>
<td align="left" width="63%">
Called to allow a system language bar item extension to add items to a system language bar menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms628959(v=VS.85).aspx">OnMenuSelect</a>
</td>
<td align="left" width="63%">
Called when the user selects an item in the system menu added by the system language bar menu extension.

</td>
</tr>
</table> 


## -remarks



A system language bar menu is an object on the language bar that supports menu items added to it by third-partyextensions. The system item must support the <a href="https://msdn.microsoft.com/en-us/library/ms628941(v=VS.85).aspx">ITfSource</a> interface and support the IID_ITfSystemLangBarItemSink identifier in its <b>ITfSource::AdviseSink</b> implementation. The system item should also implement the <a href="https://msdn.microsoft.com/en-us/library/ms628956(v=VS.85).aspx">ITfSystemLangBarItem</a> interface. The system item uses the <b>ITfSystemLangBarItemSink</b> interface to allow the extension to add its items.




## -see-also




<a href="https://msdn.microsoft.com/16612641-2bff-4e6f-a955-85793021a20b">ITfLangBarItem
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms628941(v=VS.85).aspx">ITfSource</a>



<a href="https://msdn.microsoft.com/en-us/library/ms628945(v=VS.85).aspx">ITfSource::AdviseSink</a>



<a href="https://msdn.microsoft.com/9b41e787-eb90-4858-8838-8c36c7dce0c1">ITfSystemLangBarItem
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

