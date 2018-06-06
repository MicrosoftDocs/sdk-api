---
UID: NF:msctf.ITfRange.ShiftEndToRange
title: ITfRange::ShiftEndToRange
author: windows-sdk-content
description: ITfRange::ShiftEndToRange method
old-location: tsf\itfrange_shiftendtorange.htm
old-project: TSF
ms.assetid: 27595909-025b-46c9-bd6f-2e64a720c97c
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITfRange interface [Text Services Framework],ShiftEndToRange method, ITfRange.ShiftEndToRange, ITfRange::ShiftEndToRange, ShiftEndToRange, ShiftEndToRange method [Text Services Framework], ShiftEndToRange method [Text Services Framework],ITfRange interface, _tsf_itfrange_shiftendtorange_ref, msctf/ITfRange::ShiftEndToRange, tsf.itfrange_shiftendtorange
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
 - ITfRange.ShiftEndToRange
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfRange::ShiftEndToRange


## -description




## -parameters




### -param ec [in]

Contains an edit cookie that identifies the edit context obtained from <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> or <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param pRange [in]

Pointer to an <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> interface that contains the anchor that the end anchor is moved to.


### -param aPos [in]

Contains one of the <a href="https://msdn.microsoft.com/d670666f-2915-4a23-b825-b534a015e37f">TfAnchor</a> values that specify which anchor of <i>pRange</i> the end anchor will get moved to.


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

If the shift operation causes the range end anchor to move past the start anchor, the start anchor is moved to the same location as the end anchor.

This method is more efficient than <a href="https://msdn.microsoft.com/1debec6d-f98f-45a4-aaa8-99b61f3583ef">ITfRange::ShiftEnd</a> and should be used.




## -see-also




<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">
        ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">
        ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">
        ITfRange
      </a>



<a href="https://msdn.microsoft.com/1debec6d-f98f-45a4-aaa8-99b61f3583ef">
        ITfRange::ShiftEnd
      </a>



<a href="https://msdn.microsoft.com/8e3e40a0-71ba-4abf-ac99-99d66856746c">
        ITfRange::ShiftStartToRange
      </a>
 

 

