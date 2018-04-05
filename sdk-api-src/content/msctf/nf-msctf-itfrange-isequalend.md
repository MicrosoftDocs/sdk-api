---
UID: NF:msctf.ITfRange.IsEqualEnd
title: ITfRange::IsEqualEnd method
author: windows-driver-content
description: The ITfRange::IsEqualStart method verifies that the end anchor of this range of text matches an anchor of another specified range.
old-location: tsf\itfrange_isequalend.htm
old-project: TSF
ms.assetid: 03b87230-457f-4483-a183-d8a8cc7cead4
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfRange, ITfRange interface [Text Services Framework], IsEqualEnd method, ITfRange::IsEqualEnd, IsEqualEnd method [Text Services Framework], IsEqualEnd method [Text Services Framework], ITfRange interface, IsEqualEnd,ITfRange.IsEqualEnd, TF_ANCHOR_END, TF_ANCHOR_START, _tsf_itfrange_isequalend_ref, msctf/ITfRange::IsEqualEnd, tsf.itfrange_isequalend
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
-	ITfRange.IsEqualEnd
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfRange::IsEqualEnd method


## -description


The <a href="https://msdn.microsoft.com/562c2821-9522-4fb5-ae15-4430cd2711c6">ITfRange::IsEqualStart</a> method verifies that the end anchor of this range of text matches an anchor of another specified range.


## -parameters




### -param ec [in]

Edit cookie obtained from <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> or <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param pWith [in]

Pointer to a specified range in which an anchor is to be compared to this range end anchor.


### -param aPos [in]

Enumeration element that indicates which anchor of the specified <i>pWith</i> range to compare with this range end anchor.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_ANCHOR_START"></a><a id="tf_anchor_start"></a><dl>
<dt><b>TF_ANCHOR_START</b></dt>
</dl>
</td>
<td width="60%">
Compares this range end anchor with the specified range start anchor.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_ANCHOR_END"></a><a id="tf_anchor_end"></a><dl>
<dt><b>TF_ANCHOR_END</b></dt>
</dl>
</td>
<td width="60%">
Compares this range end anchor with the specified range end anchor.

</td>
</tr>
</table>
 


### -param pfEqual [out]

Pointer to a Boolean value. Upon return, <b>TRUE</b> indicates that the specified <i>pWith</i> range anchor matches this range end anchor. <b>FALSE</b> indicates otherwise.


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
 




## -remarks



This method is identical to <b>ITfRange::IsEqualStart</b>, except that the end anchor of this range is compared to an anchor of another specified range.

This method is functionally equivalent to, but more efficient than, <a href="https://msdn.microsoft.com/23841f07-f2ea-4365-a8cb-128c4fb210ab">ITfRange::CompareEnd</a>.




## -see-also




<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">
        ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a>



<a href="https://msdn.microsoft.com/23841f07-f2ea-4365-a8cb-128c4fb210ab">
        ITfRange::CompareEnd
      </a>



<a href="https://msdn.microsoft.com/562c2821-9522-4fb5-ae15-4430cd2711c6">
        ITfRange:IsEqualStart
      </a>



<a href="https://msdn.microsoft.com/c827999a-0b74-4e5d-901e-4c2fa1d74929">Text Stores</a>



<a href="https://msdn.microsoft.com/d670666f-2915-4a23-b825-b534a015e37f">
        TfAnchor
      </a>
 

 

