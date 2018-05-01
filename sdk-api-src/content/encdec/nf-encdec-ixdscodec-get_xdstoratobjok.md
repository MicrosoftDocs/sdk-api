---
UID: NF:encdec.IXDSCodec.get_XDSToRatObjOK
title: IXDSCodec::get_XDSToRatObjOK method
author: windows-driver-content
description: The get_XDSToRatObjOK method queries whether the XDSToRat object was created successfully.
old-location: mstv\ixdscodec_get_xdstoratobjok.htm
old-project: mstv
ms.assetid: 846f3f68-8745-416d-9f0e-1e6ef83054b2
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IXDSCodec, IXDSCodec interface [Microsoft TV Technologies], get_XDSToRatObjOK method, IXDSCodec::get_XDSToRatObjOK, IXDSCodecXDSToRatObjOK, encdec/IXDSCodec::get_XDSToRatObjOK, get_XDSToRatObjOK method [Microsoft TV Technologies], get_XDSToRatObjOK method [Microsoft TV Technologies], IXDSCodec interface, get_XDSToRatObjOK,IXDSCodec.get_XDSToRatObjOK, mstv.ixdscodec_get_xdstoratobjok
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ProtType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	EncDec.h
api_name:
-	IXDSCodec.get_XDSToRatObjOK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IXDSCodec::get_XDSToRatObjOK method


## -description


The <b>get_XDSToRatObjOK</b> method queries whether the <b>XDSToRat</b> object was created successfully.


## -parameters




### -param pHrCoCreateRetVal [out, retval]

Receives an <b>HRESULT</b> value. The <b>HRESULT</b> is the value that was returned when the filter called <b>CoCreateInstance</b> to create the <b>XDSToRat</b> object. If it equals S_OK, the <b>EvalRat</b> object was created successfully.


## -returns



Returns an <b>HRESULT</b>. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c34a3418-2ae5-45a6-9e3b-2bd7cf33d44b">IXDSCodec Interface</a>
 

 

