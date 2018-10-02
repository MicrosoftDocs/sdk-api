---
UID: NF:textstor.ITextStoreAnchor.GetWnd
title: ITextStoreAnchor::GetWnd
author: windows-sdk-content
description: The ITextStoreAnchor::GetWnd method returns the handle to a window that corresponds to the current text stream.
old-location: tsf\itextstoreanchor_getwnd.htm
tech.root: TSF
ms.assetid: e77b5218-45e4-4fe1-a41f-1d7b5887ba30
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetWnd, GetWnd method [Text Services Framework], GetWnd method [Text Services Framework],ITextStoreAnchor interface, ITextStoreAnchor interface [Text Services Framework],GetWnd method, ITextStoreAnchor.GetWnd, ITextStoreAnchor::GetWnd, textstor/ITextStoreAnchor::GetWnd, tsf.itextstoreanchor_getwnd
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
 - ITextStoreAnchor.GetWnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreAnchor::GetWnd


## -description


The <b>ITextStoreAnchor::GetWnd</b> method returns the handle to a window that corresponds to the current text stream.


## -parameters




### -param vcView [in]

Specifies the <a href="https://msdn.microsoft.com/e649b799-d0d6-4f2d-b9f1-28070eea9b16">TsViewCookie</a> data type that corresponds to the current document.


### -param phwnd [out]

Receives a pointer to the handle of the window that corresponds to the current document. This parameter can be <b>NULL</b> if the document does not have the corresponding handle to the window.


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
The <b>TsViewCookie</b> data type is invalid.

</td>
</tr>
</table>
 




## -remarks



A document might not have a corresponding window handle if the document is in memory but not displayed on the screen, or if the document is a windowless control and the control does not recognize the window handle of the owner of the windowless controls. Callers cannot assume that the <i>phwnd</i> parameter will receive a non-<b>NULL</b> value even if the method is successful. Callers can also receive a <b>NULL</b> value for the <i>phwnd</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a>



<a href="https://msdn.microsoft.com/e649b799-d0d6-4f2d-b9f1-28070eea9b16">TsViewCookie
      </a>
 

 

