---
UID: NN:sbe.IStreamBufferRecComp
title: IStreamBufferRecComp (sbe.h)
description: The IStreamBufferRecComp interface is used to create new content recordings by concatenating existing recordings. The new recording can be created from a mix of reference and content recordings.The Stream Buffer RecComp object exposes this interface.
helpviewer_keywords: ["IStreamBufferRecComp","IStreamBufferRecComp interface [Microsoft TV Technologies]","IStreamBufferRecComp interface [Microsoft TV Technologies]","described","IStreamBufferRecCompInterface","mstv.istreambufferreccomp","sbe/IStreamBufferRecComp"]
old-location: mstv\istreambufferreccomp.htm
tech.root: mstv
ms.assetid: 2998d606-d5ee-4dc3-a4da-57c597c6b594
ms.date: 12/05/2018
ms.keywords: IStreamBufferRecComp, IStreamBufferRecComp interface [Microsoft TV Technologies], IStreamBufferRecComp interface [Microsoft TV Technologies],described, IStreamBufferRecCompInterface, mstv.istreambufferreccomp, sbe/IStreamBufferRecComp
req.header: sbe.h
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
 - IStreamBufferRecComp
 - sbe/IStreamBufferRecComp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferRecComp
---

# IStreamBufferRecComp interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IStreamBufferRecComp</b> interface is used to create new content recordings by concatenating existing recordings. The new recording can be created from a mix of reference and content recordings.

The Stream Buffer <a href="/previous-versions/windows/desktop/mstv/reccomp-object">RecComp</a> object exposes this interface.

## -inheritance

The <b>IStreamBufferRecComp</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStreamBufferRecComp</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferRecComp)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>
