---
UID: NF:encdec.IDTFilter.put_BlockedRatingAttributes
title: IDTFilter::put_BlockedRatingAttributes (encdec.h)
author: windows-sdk-content
description: The put_BlockedRatingAttributes method specifies whether to block content that has a specified rating.
old-location: mstv\idtfilter_put_blockedratingattributes.htm
tech.root: mstv
ms.assetid: ae81e427-305e-43b8-ad4d-e23f0bbbdc4a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDTFilter interface [Microsoft TV Technologies],put_BlockedRatingAttributes method, IDTFilter.put_BlockedRatingAttributes, IDTFilter::put_BlockedRatingAttributes, IDTFilterput_BlockedRatingAttributes, encdec/IDTFilter::put_BlockedRatingAttributes, mstv.idtfilter_put_blockedratingattributes, put_BlockedRatingAttributes, put_BlockedRatingAttributes method [Microsoft TV Technologies], put_BlockedRatingAttributes method [Microsoft TV Technologies],IDTFilter interface
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
 - IDTFilter.put_BlockedRatingAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDTFilter::put_BlockedRatingAttributes


## -description


The <b>put_BlockedRatingAttributes</b> method specifies whether to block content that has a specified rating.


## -parameters




### -param enSystem [in]

Specifies the rating system, as an <a href="https://msdn.microsoft.com/646927ad-569a-4484-a3ce-6d121210b6be">EnTvRat_System</a> enumeration type.


### -param enLevel [in]

Specifies the rating level, as an <a href="https://msdn.microsoft.com/f96a8f1a-d8e2-4976-92e3-719f0039d2a8">EnTvRat_GenericLevel</a> enumeration type.


### -param lbfAttrs [in]

Bitwise combination of zero or more flags from the <a href="https://msdn.microsoft.com/eb7f56c4-1d48-43f9-a691-c08aee3cd537">BfEnTvRat_GenericAttributes</a> enumeration.


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



The filter passes this call through to the <b>EvalRat</b> object. For more information, see <a href="https://msdn.microsoft.com/7c6919f0-1270-4dcd-8180-a9af4763c580">IEvalRat::put_BlockedRatingAttributes</a>.




## -see-also




<a href="https://msdn.microsoft.com/15acf764-7e4d-40c3-b907-ff5dfaa69dae">IDTFilter Interface</a>
 

 

