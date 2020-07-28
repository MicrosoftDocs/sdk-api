---
UID: NF:strmif.IEnumPins.Next
title: IEnumPins::Next (strmif.h)
description: The Next method retrieves a specified number of pins in the enumeration sequence.
helpviewer_keywords: ["IEnumPins interface [DirectShow]","Next method","IEnumPins.Next","IEnumPins::Next","IEnumPinsNext","Next","Next method [DirectShow]","Next method [DirectShow]","IEnumPins interface","dshow.ienumpins_next","strmif/IEnumPins::Next"]
old-location: dshow\ienumpins_next.htm
tech.root: dshow
ms.assetid: 03a30eb6-b39f-4497-ad3f-8af2c3ecf2f0
ms.date: 12/05/2018
ms.keywords: IEnumPins interface [DirectShow],Next method, IEnumPins.Next, IEnumPins::Next, IEnumPinsNext, Next, Next method [DirectShow], Next method [DirectShow],IEnumPins interface, dshow.ienumpins_next, strmif/IEnumPins::Next
f1_keywords:
- strmif/IEnumPins.Next
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IEnumPins.Next
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumPins::Next


## -description



The <code>Next</code> method retrieves a specified number of pins in the enumeration sequence.




## -parameters




### -param cPins [in]

Number of pins to retrieve.


### -param ppPins [out]

Array of size <i>cPins</i> that is filled with <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> pointers. The caller must release the interfaces.


### -param pcFetched [out]

Pointer to a variable that receives the number of pins retrieved. Can be <b>NULL</b> if <i>cPins</i> is 1.


## -returns



Returns one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Did not retrieve as many pins as requested.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_ENUM_OUT_OF_SYNC</b></dt>
</dl>
</td>
<td width="60%">
The filter's state has changed and is now inconsistent with the enumerator.

</td>
</tr>
</table>
 




## -remarks



This method retrieves pointers to the specified number of pins, starting at the current position in the enumeration, and places them in the specified array.

If the method succeeds, the <b>IPin</b> pointers all have outstanding reference counts. Be sure to release them when you are done.

If the number of pins changes, the enumerator is no longer consistent with the filter, and the method returns VFW_E_ENUM_OUT_OF_SYNC. Discard any data obtained from previous calls to the enumerator, because it might be invalid. Update the enumerator by calling the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienumpins-reset">IEnumPins::Reset</a> method. You can then call the <code>Next</code> method safely.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ienumpins">IEnumPins Interface</a>
 

 

