---
UID: NN:ctffunc.ITfFnBalloon
title: ITfFnBalloon
author: windows-driver-content
description: The ITfFnBalloon interface is implemented by a text service and is used by an application or other text service to update the balloon item that the text service adds to the language bar.
old-location: tsf\itffnballoon.htm
old-project: TSF
ms.assetid: 9b79526b-b7e1-41a2-b32e-88124347d77d
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfFnBalloon, ITfFnBalloon interface [Text Services Framework], ITfFnBalloon interface [Text Services Framework], described, _tsf_itffnballoon_ref, ctffunc/ITfFnBalloon, tsf.itffnballoon
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TfIntegratableCandidateListSelectionStyle
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfFnBalloon
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfFnBalloon interface


## -description


The <b>ITfFnBalloon</b> interface is implemented by a text service and is used by an application or other text service to update the balloon item that the text service adds to the language bar.

An application or text service obtains an instance of this interface by calling <a href="https://msdn.microsoft.com/b320790a-4b54-4475-97e6-e59f083cfc09">ITfThreadMgr::GetFunctionProvider</a> with the class identifier of the text service and then calling <a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">ITfFunctionProvider::GetFunction</a> with GUID_NULL and IID_ITfFnBalloon.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfFnBalloon</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfFnBalloon</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfFnBalloon</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b395d587-02a7-496e-8bfd-8fcaba2a3edc">UpdateBalloon</a>
</td>
<td align="left" width="63%">
Changes the style and text of a language bar balloon item.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a8ec629a-9ac6-4f25-82f2-42af6ce52ddc">ITfFunctionProvider::GetFunction</a>



<a href="https://msdn.microsoft.com/b320790a-4b54-4475-97e6-e59f083cfc09">ITfThreadMgr::GetFunctionProvider</a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

