---
UID: NF:mediaobj.IMediaObjectInPlace.Process
title: IMediaObjectInPlace::Process (mediaobj.h)
description: The Process method processes a block of data. The application supplies a pointer to a block of input data. The DMO processes the data in place.helpviewer_keywords: ["IMediaObjectInPlace interface [DirectShow]","Process method","IMediaObjectInPlace.Process","IMediaObjectInPlace::Process","IMediaObjectInPlaceProcess","Process","Process method [DirectShow]","Process method [DirectShow]","IMediaObjectInPlace interface","dshow.imediaobjectinplace_process","mediaobj/IMediaObjectInPlace::Process"]
old-location: dshow\imediaobjectinplace_process.htm
tech.root: DirectShow
ms.assetid: 567117cd-db7b-4764-9c88-ab898a64b56a
ms.date: 12/05/2018
ms.keywords: IMediaObjectInPlace interface [DirectShow],Process method, IMediaObjectInPlace.Process, IMediaObjectInPlace::Process, IMediaObjectInPlaceProcess, Process, Process method [DirectShow], Process method [DirectShow],IMediaObjectInPlace interface, dshow.imediaobjectinplace_process, mediaobj/IMediaObjectInPlace::Process
f1_keywords:
- mediaobj/IMediaObjectInPlace.Process
dev_langs:
- c++
req.header: mediaobj.h
req.include-header: Dmo.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Dmoguids.lib
- Dmoguids.dll
api_name:
- IMediaObjectInPlace.Process
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaObjectInPlace::Process


## -description



The <code>Process</code> method processes a block of data. The application supplies a pointer to a block of input data. The DMO processes the data in place.




## -parameters




### -param ulSize [in]

Size of the data, in bytes.


### -param pData [in, out]

Pointer to a buffer of size <i>ulSize</i>. On input, the buffer holds the input data. If the method returns successfully, the buffer contains the output data.


### -param refTimeStart [in]

Start time of the data.


### -param dwFlags [in]

Either DMO_INPLACE_NORMAL or DMO_INPLACE_ZERO. See Remarks for more information.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Success. There is still data to process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success. There is no remaining data to process.

</td>
</tr>
</table>
 




## -remarks



If the method fails, the buffer might contain garbage. The application should not use the contents of the buffer.

The DMO might produce output data beyond the length of the input data. This is called an <i>effect tail</i>. For example, a reverb effect continues after the input reaches silence. If the DMO has an effect tail, this method returns S_FALSE.

While the application has input data for processing, call the <code>Process</code> method with the <i>dwFlags</i> parameter set to DMO_INPLACE_NORMAL. If the last such call returns S_FALSE, call <code>Process</code> again, this time with a zeroed input buffer and the DMO_INPLACE_ZERO flag. The DMO will now fill the zeroed buffer with the effect tail. Continue calling <code>Process</code> in this way until the return value is S_OK, indicating that the DMO has finished processing the effect tail.

If the DMO has no effect tail, this method returns S_TRUE or an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace">IMediaObjectInPlace Interface</a>
 

 

