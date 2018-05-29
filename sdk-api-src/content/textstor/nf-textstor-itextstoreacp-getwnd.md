---
UID: NF:textstor.ITextStoreACP.GetWnd
title: ITextStoreACP::GetWnd
author: windows-sdk-content
description: The ITextStoreACP::GetWnd method returns the handle to a window that corresponds to the current document.
old-location: tsf\itextstoreacp_getwnd.htm
old-project: TSF
ms.assetid: 7fb49702-4e0e-4e8c-9227-83c0b014f5f2
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetWnd, GetWnd method [Text Services Framework], GetWnd method [Text Services Framework],ITextStoreACP interface, ITextStoreACP interface [Text Services Framework],GetWnd method, ITextStoreACP.GetWnd, ITextStoreACP::GetWnd, _tsf_itextstoreacp_getwnd_ref, textstor/ITextStoreACP::GetWnd, tsf.itextstoreacp_getwnd
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
-	ITextStoreACP.GetWnd
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACP::GetWnd


## -description


The <b>ITextStoreACP::GetWnd</b> method returns the handle to a window that corresponds to the current document.


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



A document cannot have a corresponding window handle if the document is in memory but not displayed on the screen, or if the document is a windowless control and the control does not recognize the window handle of the owner of the windowless controls. Callers cannot assume that the <i>phwnd</i> parameter will receive a non-<b>NULL</b> value even if the method is successful. Callers can also receive a <b>NULL</b> value for the <i>phwnd</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a>



<a href="https://msdn.microsoft.com/e649b799-d0d6-4f2d-b9f1-28070eea9b16">TsViewCookie
      </a>
 

 

