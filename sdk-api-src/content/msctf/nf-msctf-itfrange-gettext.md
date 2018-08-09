---
UID: NF:msctf.ITfRange.GetText
title: ITfRange::GetText
author: windows-sdk-content
description: The ITfRange::GetText method obtains the content covered by this range of text.
old-location: tsf\itfrange_gettext.htm
old-project: TSF
ms.assetid: b38a8de3-947f-469c-9f0d-f0482ea86884
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetText, GetText method [Text Services Framework], GetText method [Text Services Framework],ITfRange interface, ITfRange interface [Text Services Framework],GetText method, ITfRange.GetText, ITfRange::GetText, TF_TF_IGNOREEND, TF_TF_MOVESTART, _tsf_itfrange_gettext_ref, msctf/ITfRange::GetText, tsf.itfrange_gettext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfRange.GetText
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfRange::GetText


## -description


The <b>ITfRange::GetText</b> method obtains the content covered by this range of text.


## -parameters




### -param ec [in]

Edit cookie that identifies the edit context obtained from <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> or <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param dwFlags [in]

Bit fields that specify optional behavior.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_TF_MOVESTART"></a><a id="tf_tf_movestart"></a><dl>
<dt><b>TF_TF_MOVESTART</b></dt>
</dl>
</td>
<td width="60%">
Start anchor of the range is advanced to the position after the last character returned.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TF_IGNOREEND"></a><a id="tf_tf_ignoreend"></a><dl>
<dt><b>TF_TF_IGNOREEND</b></dt>
</dl>
</td>
<td width="60%">
Method attempts to fill <i>pchText</i> with the maximum number of characters, instead of halting the copy at the position occupied by the end anchor of the range.

</td>
</tr>
</table>
 


### -param pchText [out]

Pointer to a buffer to receive the text in the range.


### -param cchMax [in]

Maximum size of the text buffer.


### -param pcch [out]

Pointer to a ULONG representing the number of characters written to the <i>pchText</i> text buffer.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

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
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The value of the <i>ec</i> parameter is an invalid cookie, or the caller does not have a read-only lock.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a>



<a href="https://msdn.microsoft.com/1b779d99-3e09-4789-8575-73a6ecb44e3b">TF_TF_* Constants</a>



<a href="https://msdn.microsoft.com/c827999a-0b74-4e5d-901e-4c2fa1d74929">Text Stores</a>
 

 

