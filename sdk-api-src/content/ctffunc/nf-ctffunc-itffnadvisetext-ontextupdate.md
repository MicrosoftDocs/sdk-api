---
UID: NF:ctffunc.ITfFnAdviseText.OnTextUpdate
title: ITfFnAdviseText::OnTextUpdate
author: windows-sdk-content
description: ITfFnAdviseText::OnTextUpdate method
old-location: tsf\itffnadvisetext_ontextupdate.htm
old-project: TSF
ms.assetid: 0b8235bd-22a6-4074-89e5-2223a20f3559
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITfFnAdviseText interface [Text Services Framework],OnTextUpdate method, ITfFnAdviseText.OnTextUpdate, ITfFnAdviseText::OnTextUpdate, OnTextUpdate, OnTextUpdate method [Text Services Framework], OnTextUpdate method [Text Services Framework],ITfFnAdviseText interface, _tsf_itffnadvisetext_ontextupdate_ref, ctffunc/ITfFnAdviseText::OnTextUpdate, tsf.itffnadvisetext_ontextupdate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TfIntegratableCandidateListSelectionStyle
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfFnAdviseText.OnTextUpdate
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfFnAdviseText::OnTextUpdate


## -description




## -parameters




### -param pRange [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> object that represents the range of text that has changed.


### -param pchText [in]

Pointer to a <b>WCHAR</b> buffer that contains the new text for the range.


### -param cch [in]

Specifies the number of characters contained in <i>pchText</i>.


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




<a href="https://msdn.microsoft.com/7cca7f23-48d3-4855-8f3d-e937bbc990d4">ITfFnAdviseText</a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>
 

 

