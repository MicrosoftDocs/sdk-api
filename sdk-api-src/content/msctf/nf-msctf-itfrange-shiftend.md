---
UID: NF:msctf.ITfRange.ShiftEnd
title: ITfRange::ShiftEnd
author: windows-sdk-content
description: ITfRange::ShiftEnd method
old-location: tsf\itfrange_shiftend.htm
old-project: TSF
ms.assetid: 1debec6d-f98f-45a4-aaa8-99b61f3583ef
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: ITfRange interface [Text Services Framework],ShiftEnd method, ITfRange.ShiftEnd, ITfRange::ShiftEnd, ShiftEnd, ShiftEnd method [Text Services Framework], ShiftEnd method [Text Services Framework],ITfRange interface, _tsf_itfrange_shiftend_ref, msctf/ITfRange::ShiftEnd, tsf.itfrange_shiftend
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
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfRange.ShiftEnd
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfRange::ShiftEnd


## -description




## -parameters




### -param ec [in]

Contains an edit cookie that identifies the edit context. This is obtained from <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> or <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param cchReq [in]

Contains the number of characters that the end anchor is shifted. A negative value causes the anchor to move backward and a positive value causes the anchor to move forward.


### -param pcch [out]

Pointer to a <b>LONG</b> value that receives the number of characters the anchor shifted.


### -param pHalt [in]

Pointer to a <a href="https://msdn.microsoft.com/055f3228-1e3b-4e31-9035-e509a98016a8">TF_HALTCOND</a> structure that contains conditions on the shift. This parameter is optional and can be <b>NULL</b>.


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
The edit context identified by <i>ec</i> does not have a read-only lock.

</td>
</tr>
</table>
 




## -remarks



The start and end positions of a range are called anchors.

This method cannot move an anchor beyond a region boundary. If the shift reaches a region boundary, the number of characters actually shifted will be less than requested. <a href="https://msdn.microsoft.com/cda2282f-3d3c-4763-9892-b889b29963a6">ITfRange::ShiftEndRegion</a> is used to shift the anchor to an adjacent region.

If the shift operation causes the range end anchor to move past the start anchor, the start anchor is moved to the same location as the end anchor.


        ITfRange::ShiftEnd can be a lengthy operation. For better performance, use <a href="https://msdn.microsoft.com/8e3e40a0-71ba-4abf-ac99-99d66856746c">ITfRange::ShiftEndToRange</a> when possible.




## -see-also




<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">
        ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">
        ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a>



<a href="https://msdn.microsoft.com/cda2282f-3d3c-4763-9892-b889b29963a6">
        ITfRange::ShiftEndRegion
      </a>



<a href="https://msdn.microsoft.com/f9f983b1-a5fa-4857-b73c-b879c566d6f6">
        ITfRange::ShiftStart
      </a>



<a href="https://msdn.microsoft.com/055f3228-1e3b-4e31-9035-e509a98016a8">
        TF_HALTCOND
      </a>
 

 

