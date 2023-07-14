---
UID: NF:tvratings.IXDSToRat.Init
title: IXDSToRat::Init (tvratings.h)
description: The Init method sets the XDSToRat object to its initial state.
helpviewer_keywords: ["IXDSToRat interface [Microsoft TV Technologies]","Init method","IXDSToRat.Init","IXDSToRat::Init","IXDSToRatInit","Init","Init method [Microsoft TV Technologies]","Init method [Microsoft TV Technologies]","IXDSToRat interface","mstv.ixdstorat_init","tvratings/IXDSToRat::Init"]
old-location: mstv\ixdstorat_init.htm
tech.root: mstv
ms.assetid: c7c38755-46d3-4100-ba14-c153c4a6a517
ms.date: 12/05/2018
ms.keywords: IXDSToRat interface [Microsoft TV Technologies],Init method, IXDSToRat.Init, IXDSToRat::Init, IXDSToRatInit, Init, Init method [Microsoft TV Technologies], Init method [Microsoft TV Technologies],IXDSToRat interface, mstv.ixdstorat_init, tvratings/IXDSToRat::Init
req.header: tvratings.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXDSToRat::Init
 - tvratings/IXDSToRat::Init
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tvratings.h
api_name:
 - IXDSToRat.Init
---

# IXDSToRat::Init


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Init</b> method sets the <a href="/previous-versions/windows/desktop/mstv/xdstorat-object">XDSToRat</a> object to its initial state.



## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

The XDS Codec filter calls this method on startup or after a discontinuity, such as a channel change. The <a href="/previous-versions/windows/desktop/mstv/xdstorat-object">XDSToRat</a> object should clear any internal buffers and reset its parsing state. This method prevents decoding errors caused by channel changes or other interruptions.

## -see-also

<a href="/previous-versions/windows/desktop/api/tvratings/nn-tvratings-ixdstorat">IXDSToRat Interface</a>
