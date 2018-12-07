---
UID: NF:msctf.ITfRange.CompareEnd
title: ITfRange::CompareEnd
author: windows-sdk-content
description: The ITfRange::CompareEnd method compares the end anchor position of this range of text to an anchor in another range.
old-location: tsf\itfrange_compareend.htm
tech.root: TSF
ms.assetid: 23841f07-f2ea-4365-a8cb-128c4fb210ab
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "+1, -1, 0, CompareEnd, CompareEnd method [Text Services Framework], CompareEnd method [Text Services Framework],ITfRange interface, ITfRange interface [Text Services Framework],CompareEnd method, ITfRange.CompareEnd, ITfRange::CompareEnd, TF_ANCHOR_END, TF_ANCHOR_START, _tsf_itfrange_compareend_ref, msctf/ITfRange::CompareEnd, tsf.itfrange_compareend"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfRange.CompareEnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfRange::CompareEnd


## -description


The <b>ITfRange::CompareEnd</b> method compares the end anchor position of this range of text to an anchor in another range.


## -parameters




### -param ec [in]

Edit cookie obtained from <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> or <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param pWith [in]

Pointer to a specified range in which an anchor is to be compared with this range end anchor.


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
Compare this range end anchor with the specified range start anchor.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_ANCHOR_END"></a><a id="tf_anchor_end"></a><dl>
<dt><b>TF_ANCHOR_END</b></dt>
</dl>
</td>
<td width="60%">
Compare this range end anchor with the specified range end anchor.

</td>
</tr>
</table>
 


### -param plResult [out]

Pointer to the result of the comparison between this range end anchor and the anchor of the specified <i>pWith</i> range.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="-1"></a><dl>
<dt><b>-1</b></dt>
</dl>
</td>
<td width="60%">
This end anchor is behind the anchor of the specified range (position of this end anchor &lt; position of the anchor of the specified range).

</td>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
This end anchor is at the same position as the anchor of the specified range.

</td>
</tr>
<tr>
<td width="40%"><a id="_1"></a><dl>
<dt><b>+1</b></dt>
</dl>
</td>
<td width="60%">
This end anchor is ahead of the anchor of the specified range (position of this end anchor &gt; position of the anchor of the specified range).

</td>
</tr>
</table>
 


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



This method will never return 0 unless the two anchors are in a single region. If the caller only requires information about whether the two anchors are positioned at the same location, <a href="https://msdn.microsoft.com/03b87230-457f-4483-a183-d8a8cc7cead4">ITfRange::IsEqualEnd</a> is more efficient.

This method is identical to <a href="https://msdn.microsoft.com/562c2821-9522-4fb5-ae15-4430cd2711c6">ITfRange::CompareStart</a>, except that the end anchor of this range is compared to an anchor of another specified range.




## -see-also




<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a>



<a href="https://msdn.microsoft.com/b84375ec-e00a-4cb3-97b7-f10688814968">ITfRange::CompareStart
      </a>



<a href="https://msdn.microsoft.com/03b87230-457f-4483-a183-d8a8cc7cead4">ITfRange::IsEqualEnd
      </a>



<a href="https://msdn.microsoft.com/c827999a-0b74-4e5d-901e-4c2fa1d74929">Text Stores</a>



<a href="https://msdn.microsoft.com/d670666f-2915-4a23-b825-b534a015e37f">TfAnchor
      </a>
 

 

