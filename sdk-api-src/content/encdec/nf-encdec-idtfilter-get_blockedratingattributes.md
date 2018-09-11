---
UID: NF:encdec.IDTFilter.get_BlockedRatingAttributes
title: IDTFilter::get_BlockedRatingAttributes
author: windows-sdk-content
description: The get_BlockedRatingAttributes method determines whether content is blocked for a given rating system and rating level.
old-location: mstv\idtfilter_get_blockedratingattributes.htm
tech.root: mstv
ms.assetid: cf7a5596-3d10-4ce9-a8c8-2703cf1eb7f8
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IDTFilter interface [Microsoft TV Technologies],get_BlockedRatingAttributes method, IDTFilter.get_BlockedRatingAttributes, IDTFilter::get_BlockedRatingAttributes, IDTFilterget_BlockedRatingAttributes, encdec/IDTFilter::get_BlockedRatingAttributes, get_BlockedRatingAttributes, get_BlockedRatingAttributes method [Microsoft TV Technologies], get_BlockedRatingAttributes method [Microsoft TV Technologies],IDTFilter interface, mstv.idtfilter_get_blockedratingattributes
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EncDec.h
api_name:
 - IDTFilter.get_BlockedRatingAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDTFilter::get_BlockedRatingAttributes


## -description


The <b>get_BlockedRatingAttributes</b> method determines whether content is blocked for a given rating system and rating level.


## -parameters




### -param enSystem

TBD


### -param enLevel

TBD


### -param plbfEnAttr [out, retval]

Receives a bitwise combination of flags from the <a href="https://msdn.microsoft.com/eb7f56c4-1d48-43f9-a691-c08aee3cd537">BfEnTvRat_GenericAttributes</a> enumeration.


#### - EnRating [in]

Specifies the rating level as an <a href="https://msdn.microsoft.com/f96a8f1a-d8e2-4976-92e3-719f0039d2a8">EnTvRat_GenericLevel</a> enumeration type.


#### - EnSystem [in]

Specifies the rating system as an <a href="https://msdn.microsoft.com/646927ad-569a-4484-a3ce-6d121210b6be">EnTvRat_System</a> enumeration type.


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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The <b>EvalRat</b> object was not successfully created.

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
</table>
 




## -remarks



The filter passes this call through to the <b>EvalRat</b> object. For more information, see <a href="https://msdn.microsoft.com/d07b6462-958c-4e97-9be1-41941aa6b747">IEvalRat::get_BlockedRatingAttributes</a>.




## -see-also




<a href="https://msdn.microsoft.com/15acf764-7e4d-40c3-b907-ff5dfaa69dae">IDTFilter Interface</a>
 

 

