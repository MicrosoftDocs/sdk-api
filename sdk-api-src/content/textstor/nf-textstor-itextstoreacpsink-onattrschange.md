---
UID: NF:textstor.ITextStoreACPSink.OnAttrsChange
title: ITextStoreACPSink::OnAttrsChange
author: windows-driver-content
description: ITextStoreACPSink::OnAttrsChange method
old-location: tsf\itextstoreacpsink_onattrschange.htm
old-project: TSF
ms.assetid: ae1e5f92-7462-46b4-b4dd-5032147de688
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITextStoreACPSink interface [Text Services Framework],OnAttrsChange method, ITextStoreACPSink.OnAttrsChange, ITextStoreACPSink::OnAttrsChange, OnAttrsChange, OnAttrsChange method [Text Services Framework], OnAttrsChange method [Text Services Framework],ITextStoreACPSink interface, _tsf_itextstoreacpsink_onattrschange_ref, textstor/ITextStoreACPSink::OnAttrsChange, tsf.itextstoreacpsink_onattrschange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TsRunType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITextStoreACPSink.OnAttrsChange
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACPSink::OnAttrsChange


## -description




## -parameters




### -param acpStart [in]

Specifies the starting point of the attribute change.


### -param acpEnd [in]

Specifies the ending point of the attribute change.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

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
 



