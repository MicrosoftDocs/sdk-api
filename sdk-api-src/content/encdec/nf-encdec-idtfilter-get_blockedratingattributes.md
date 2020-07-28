---
UID: NF:encdec.IDTFilter.get_BlockedRatingAttributes
title: IDTFilter::get_BlockedRatingAttributes (encdec.h)
description: The get_BlockedRatingAttributes method determines whether content is blocked for a given rating system and rating level.
helpviewer_keywords: ["IDTFilter interface [Microsoft TV Technologies]","get_BlockedRatingAttributes method","IDTFilter.get_BlockedRatingAttributes","IDTFilter::get_BlockedRatingAttributes","IDTFilterget_BlockedRatingAttributes","encdec/IDTFilter::get_BlockedRatingAttributes","get_BlockedRatingAttributes","get_BlockedRatingAttributes method [Microsoft TV Technologies]","get_BlockedRatingAttributes method [Microsoft TV Technologies]","IDTFilter interface","mstv.idtfilter_get_blockedratingattributes"]
old-location: mstv\idtfilter_get_blockedratingattributes.htm
tech.root: mstv
ms.assetid: cf7a5596-3d10-4ce9-a8c8-2703cf1eb7f8
ms.date: 12/05/2018
ms.keywords: IDTFilter interface [Microsoft TV Technologies],get_BlockedRatingAttributes method, IDTFilter.get_BlockedRatingAttributes, IDTFilter::get_BlockedRatingAttributes, IDTFilterget_BlockedRatingAttributes, encdec/IDTFilter::get_BlockedRatingAttributes, get_BlockedRatingAttributes, get_BlockedRatingAttributes method [Microsoft TV Technologies], get_BlockedRatingAttributes method [Microsoft TV Technologies],IDTFilter interface, mstv.idtfilter_get_blockedratingattributes
f1_keywords:
- encdec/IDTFilter.get_BlockedRatingAttributes
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
- IDTFilter.get_BlockedRatingAttributes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDTFilter::get_BlockedRatingAttributes


## -description


The <b>get_BlockedRatingAttributes</b> method determines whether content is blocked for a given rating system and rating level.


## -parameters




### -param enSystem [in]

Specifies the rating system as an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/ne-tvratings-entvrat_system">EnTvRat_System</a> enumeration type.


### -param enLevel [in]

Specifies the rating level as an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/ne-tvratings-entvrat_genericlevel">EnTvRat_GenericLevel</a> enumeration type.


### -param plbfEnAttr [out, retval]

Receives a bitwise combination of flags from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/ne-tvratings-bfentvrat_genericattributes">BfEnTvRat_GenericAttributes</a> enumeration.


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



The filter passes this call through to the <b>EvalRat</b> object. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/nf-tvratings-ievalrat-get_blockedratingattributes">IEvalRat::get_BlockedRatingAttributes</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/encdec/nn-encdec-idtfilter">IDTFilter Interface</a>
 

 

