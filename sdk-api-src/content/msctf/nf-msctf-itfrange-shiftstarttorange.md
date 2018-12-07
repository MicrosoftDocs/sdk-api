---
UID: NF:msctf.ITfRange.ShiftStartToRange
title: ITfRange::ShiftStartToRange
author: windows-sdk-content
description: ITfRange::ShiftStartToRange method
old-location: tsf\itfrange_shiftstarttorange.htm
tech.root: TSF
ms.assetid: 8e3e40a0-71ba-4abf-ac99-99d66856746c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfRange interface [Text Services Framework],ShiftStartToRange method, ITfRange.ShiftStartToRange, ITfRange::ShiftStartToRange, ShiftStartToRange, ShiftStartToRange method [Text Services Framework], ShiftStartToRange method [Text Services Framework],ITfRange interface, _tsf_itfrange_shiftstarttorange_ref, msctf/ITfRange::ShiftStartToRange, tsf.itfrange_shiftstarttorange
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
 - ITfRange.ShiftStartToRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfRange::ShiftStartToRange


## -description




## -parameters




### -param ec [in]

Contains an edit cookie that identifies the edit context obtained from <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> or <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param pRange [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> interface that contains the anchor that the start anchor is moved to.


### -param aPos [in]

Contains one of the <a href="https://msdn.microsoft.com/d670666f-2915-4a23-b825-b534a015e37f">TfAnchor</a> values that specifies which anchor of <i>pRange</i> the start anchor is moved to.


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
<i>pRange</i> is invalid.

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
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The edit context identified by <i>ec</i> does not have a read-only lock.

</td>
</tr>
</table>
 




## -remarks



The start and end positions of a range are called anchors.

If the shift operation causes the range start anchor to move past the end anchor, the end anchor is moved to the same location as the start anchor.

This method is more efficient than <a href="https://msdn.microsoft.com/f9f983b1-a5fa-4857-b73c-b879c566d6f6">ITfRange::ShiftStart</a> and should be used when possible.




## -see-also




<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>



<a href="https://msdn.microsoft.com/27595909-025b-46c9-bd6f-2e64a720c97c">ITfRange::ShiftEndToRange
      </a>



ITfRange::ShiftStart



<a href="https://msdn.microsoft.com/d670666f-2915-4a23-b825-b534a015e37f">TfAnchor
      </a>
 

 

