---
UID: NN:msctf.ITfFunctionProvider
title: ITfFunctionProvider
author: windows-driver-content
description: The ITfFunctionProvider interface is implemented by an application or text service to provide various function objects.
old-location: tsf\itffunctionprovider.htm
old-project: TSF
ms.assetid: e63fd561-1157-49b1-a981-e578d9538876
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITfFunctionProvider, ITfFunctionProvider interface [Text Services Framework], ITfFunctionProvider interface [Text Services Framework],described, _tsf_itffunctionprovider_ref, msctf/ITfFunctionProvider, tsf.itffunctionprovider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfFunctionProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfFunctionProvider interface


## -description


The <b>ITfFunctionProvider</b> interface is implemented by an application or text service to provide various function objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFunctionProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfFunctionProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFunctionProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546575">GetDescription</a>
</td>
<td align="left" width="63%">
Obtains the description of the function provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">GetFunction</a>
</td>
<td align="left" width="63%">
Obtains the specified function object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Obtains the type identifier for the function provider.

</td>
</tr>
</table> 


## -remarks



A function provider is registered by calling <a href="https://msdn.microsoft.com/d9231f36-24c4-4d46-97e7-518f5fcc1ce2">ITFSourceSingle::AdviseSingleSink</a> with IID_ITfFunctionProvider when the text service is activated. The text service should unregister its function provider with <a href="https://msdn.microsoft.com/1689dedb-c168-4a05-b598-517c87d9afbd">ITFSourceSingle::UnadviseSingleSink</a> when it is deactivated.




## -see-also




<a href="https://msdn.microsoft.com/d9231f36-24c4-4d46-97e7-518f5fcc1ce2">ITFSourceSingle::AdviseSingleSink
      </a>



<a href="https://msdn.microsoft.com/1689dedb-c168-4a05-b598-517c87d9afbd">
        ITFSourceSingle::UnadviseSingleSink
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

