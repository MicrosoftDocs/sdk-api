---
UID: NF:msctf.ITfRange.IsEmpty
title: ITfRange::IsEmpty method
author: windows-driver-content
description: The ITfRange::IsEmpty method verifies that the range of text is empty because the start and end anchors occupy the same position.
old-location: tsf\itfrange_isempty.htm
old-project: TSF
ms.assetid: 4cc720c1-acc1-445e-830e-91135fdfeeed
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfRange, ITfRange interface [Text Services Framework], IsEmpty method, ITfRange::IsEmpty, IsEmpty method [Text Services Framework], IsEmpty method [Text Services Framework], ITfRange interface, IsEmpty,ITfRange.IsEmpty, _tsf_itfrange_isempty_ref, msctf/ITfRange::IsEmpty, tsf.itfrange_isempty
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfRange.IsEmpty
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfRange::IsEmpty method


## -description


The <b>ITfRange::IsEmpty</b> method verifies that the range of text is empty because the start and end anchors occupy the same position.


## -parameters




### -param ec [in]

Edit cookie that identifies the edit context. It is obtained from <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> or <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param pfEmpty [out]

Pointer to a Boolean value. <b>TRUE</b> indicates the range is empty; <b>FALSE</b> indicates the range is not empty.


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
The value of the <i>ec</i> parameter is an invalid cookie.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">
        ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a>
 

 

