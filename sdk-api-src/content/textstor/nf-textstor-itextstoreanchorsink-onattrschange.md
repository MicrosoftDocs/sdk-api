---
UID: NF:textstor.ITextStoreAnchorSink.OnAttrsChange
title: ITextStoreAnchorSink::OnAttrsChange
author: windows-sdk-content
description: The ITextStoreAnchorSink::OnAttrsChange method is called when the value of one or more text attributes changes.
old-location: tsf\itextstoreanchorsink_onattrschange.htm
tech.root: TSF
ms.assetid: aa7226dd-1d4a-44ed-94b7-b93813bca2f8
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITextStoreAnchorSink interface [Text Services Framework],OnAttrsChange method, ITextStoreAnchorSink.OnAttrsChange, ITextStoreAnchorSink::OnAttrsChange, OnAttrsChange, OnAttrsChange method [Text Services Framework], OnAttrsChange method [Text Services Framework],ITextStoreAnchorSink interface, _tsf_itextstoreanchorsink_onattrschange_ref, textstor/ITextStoreAnchorSink::OnAttrsChange, tsf.itextstoreanchorsink_onattrschange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
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
 - ITextStoreAnchorSink.OnAttrsChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreAnchorSink::OnAttrsChange


## -description


The <b>ITextStoreAnchorSink::OnAttrsChange</b> method is called when the value of one or more text attributes changes.


## -parameters




### -param paStart [in]

Pointer to the start anchor of the range of text that has the attribute change.


### -param paEnd [in]

Pointer to the end anchor of the range of text that has the attribute change.


### -param cAttrs [in]

Specifies the number of attributes in the <i>paAttrs</i> array.


### -param paAttrs [in]

Pointer to an array of <a href="https://msdn.microsoft.com/5e375609-3d3c-4c12-ae05-dcaa70779162">TS_ATTRID</a> values that identify the attributes changed.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9bb21a4a-047e-4347-93b3-9c41cd2c20b7">ITextStoreAnchor::FindNextAttrTransition
      </a>



<a href="https://msdn.microsoft.com/d0f20507-005b-409d-90d5-5817b7d95f19">ITextStoreAnchor::RequestAttrsAtPosition
      </a>



<a href="https://msdn.microsoft.com/f0f43237-8c26-4e0c-8717-908884229b7b">ITextStoreAnchor::RequestAttrsTransitioningAtPosition
      </a>



<a href="https://msdn.microsoft.com/ab81d79d-e991-4c2d-9fb7-95393e002828">ITextStoreAnchor::RequestSupportedAttrs
      </a>



<a href="https://msdn.microsoft.com/fb96b4fb-864f-4f32-bf7c-cf7f199e552a">ITextStoreAnchorSink</a>
 

 

