---
UID: NN:msctf.ITfCompositionView
title: ITfCompositionView
author: windows-sdk-content
description: The ITfCompositionView interface is implemented by the TSF manager and used by an application to obtain data about a composition view. An instance of this interface is provided by one of the ITfContextOwnerCompositionSink methods.
old-location: tsf\itfcompositionview.htm
tech.root: TSF
ms.assetid: 1c8aac3e-384e-402e-aae8-11e240083603
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfCompositionView, ITfCompositionView interface [Text Services Framework], ITfCompositionView interface [Text Services Framework],described, _tsf_itfcompositionview_ref, msctf/ITfCompositionView, tsf.itfcompositionview
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
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
 - ITfCompositionView
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfCompositionView interface


## -description


The <b>ITfCompositionView</b> interface is implemented by the TSF manager and used by an application to obtain data about a composition view. An instance of this interface is provided by one of the <a href="https://msdn.microsoft.com/4fea0a48-df5f-4f34-a3ea-d52883f6f8b1">ITfContextOwnerCompositionSink</a> methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfCompositionView</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfCompositionView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfCompositionView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1435e083-c6a1-491c-a7c2-7d2cb1d54508">GetOwnerClsid</a>
</td>
<td align="left" width="63%">
Obtains the class identifier of the text service that created the composition object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31372688-be81-4883-9fc7-ed3f7b2f7934">GetRange</a>
</td>
<td align="left" width="63%">
Obtains a range object that contains the text covered by the composition.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/4fea0a48-df5f-4f34-a3ea-d52883f6f8b1">ITfContextOwnerCompositionSink
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

