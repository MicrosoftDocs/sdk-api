---
UID: NF:textstor.ITextStoreAnchor.GetActiveView
title: ITextStoreAnchor::GetActiveView
author: windows-sdk-content
description: The ITextStoreAnchor::GetActiveView method returns a TsViewCookie data type that specifies the current active view. TSF supports only a single active view, so a given text store should always return the same TsViewCookie data type.
old-location: tsf\itextstoreanchor_getactiveview.htm
tech.root: TSF
ms.assetid: b1940cac-7295-41c5-bd26-8be1d1fa4da9
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetActiveView, GetActiveView method [Text Services Framework], GetActiveView method [Text Services Framework],ITextStoreAnchor interface, ITextStoreAnchor interface [Text Services Framework],GetActiveView method, ITextStoreAnchor.GetActiveView, ITextStoreAnchor::GetActiveView, textstor/ITextStoreAnchor::GetActiveView, tsf.itextstoreanchor_getactiveview
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
 - ITextStoreAnchor.GetActiveView
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreAnchor::GetActiveView


## -description


The <b>ITextStoreAnchor::GetActiveView</b> method returns a <a href="https://msdn.microsoft.com/e649b799-d0d6-4f2d-b9f1-28070eea9b16">TsViewCookie</a> data type that specifies the current active view. TSF supports only a single active view, so a given text store should always return the same <b>TsViewCookie</b> data type.


## -parameters




### -param pvcView [out]

Receives the <b>TsViewCookie</b> data type that specifies the current active view.


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
<i>pvcView</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a>



<a href="https://msdn.microsoft.com/e649b799-d0d6-4f2d-b9f1-28070eea9b16">TsViewCookie
      </a>
 

 

