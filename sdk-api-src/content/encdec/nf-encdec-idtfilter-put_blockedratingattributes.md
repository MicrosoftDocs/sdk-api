---
UID: NF:encdec.IDTFilter.put_BlockedRatingAttributes
title: IDTFilter::put_BlockedRatingAttributes (encdec.h)
description: The put_BlockedRatingAttributes method specifies whether to block content that has a specified rating.
helpviewer_keywords: ["IDTFilter interface [Microsoft TV Technologies]","put_BlockedRatingAttributes method","IDTFilter.put_BlockedRatingAttributes","IDTFilter::put_BlockedRatingAttributes","IDTFilterput_BlockedRatingAttributes","encdec/IDTFilter::put_BlockedRatingAttributes","mstv.idtfilter_put_blockedratingattributes","put_BlockedRatingAttributes","put_BlockedRatingAttributes method [Microsoft TV Technologies]","put_BlockedRatingAttributes method [Microsoft TV Technologies]","IDTFilter interface"]
old-location: mstv\idtfilter_put_blockedratingattributes.htm
tech.root: mstv
ms.assetid: ae81e427-305e-43b8-ad4d-e23f0bbbdc4a
ms.date: 12/05/2018
ms.keywords: IDTFilter interface [Microsoft TV Technologies],put_BlockedRatingAttributes method, IDTFilter.put_BlockedRatingAttributes, IDTFilter::put_BlockedRatingAttributes, IDTFilterput_BlockedRatingAttributes, encdec/IDTFilter::put_BlockedRatingAttributes, mstv.idtfilter_put_blockedratingattributes, put_BlockedRatingAttributes, put_BlockedRatingAttributes method [Microsoft TV Technologies], put_BlockedRatingAttributes method [Microsoft TV Technologies],IDTFilter interface
f1_keywords:
- encdec/IDTFilter.put_BlockedRatingAttributes
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDTFilter::put_BlockedRatingAttributes


## -description


The <b>put_BlockedRatingAttributes</b> method specifies whether to block content that has a specified rating.


## -parameters




### -param enSystem [in]

Specifies the rating system, as an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/ne-tvratings-entvrat_system">EnTvRat_System</a> enumeration type.


### -param enLevel [in]

Specifies the rating level, as an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/ne-tvratings-entvrat_genericlevel">EnTvRat_GenericLevel</a> enumeration type.


### -param lbfAttrs [in]

Bitwise combination of zero or more flags from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/ne-tvratings-bfentvrat_genericattributes">BfEnTvRat_GenericAttributes</a> enumeration.


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



The filter passes this call through to the <b>EvalRat</b> object. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/nf-tvratings-ievalrat-put_blockedratingattributes">IEvalRat::put_BlockedRatingAttributes</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nn-encdec-idtfilter">IDTFilter Interface</a>
 

 

