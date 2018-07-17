---
UID: NF:msctf.ITfRange.GetFormattedText
title: ITfRange::GetFormattedText
author: windows-sdk-content
description: The ITfRange::GetFormattedText method obtains formatted content contained within a range of text. The content is packaged in an object that supports the IDataObject interface.
old-location: tsf\itfrange_getformattedtext.htm
old-project: TSF
ms.assetid: 8da4cb21-7097-4ba9-a63b-3699ef267776
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: GetFormattedText, GetFormattedText method [Text Services Framework], GetFormattedText method [Text Services Framework],ITfRange interface, ITfRange interface [Text Services Framework],GetFormattedText method, ITfRange.GetFormattedText, ITfRange::GetFormattedText, _tsf_itfrange_getformattedtext_ref, msctf/ITfRange::GetFormattedText, tsf.itfrange_getformattedtext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - ITfRange.GetFormattedText
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfRange::GetFormattedText


## -description


The <b>ITfRange::GetFormattedText</b> method obtains formatted content contained within a range of text. The content is packaged in an object that supports the <a href="https://msdn.microsoft.com/library/ms688421(v=VS.85).aspx">IDataObject</a> interface.


## -parameters




### -param ec [in]

Edit cookie obtained from <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> or <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param ppDataObject [out]

Pointer to an <b>IDataObject</b> pointer that receives an object that contains the formatted content. The formatted content is obtained using a STGMEDIUM global memory handle.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The context owner does not support exporting formatted text as an <b>IDataObject</b> object.

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
 




## -remarks



The format and storage type of the <b>IDataObject</b> are determined by the application to which the range belongs.




## -see-also




<a href="https://msdn.microsoft.com/library/ms688421(v=VS.85).aspx">IDataObject</a>



<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">
        ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a>



<a href="https://msdn.microsoft.com/c827999a-0b74-4e5d-901e-4c2fa1d74929">Text Stores</a>
 

 

