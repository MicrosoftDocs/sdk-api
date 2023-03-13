---
UID: NN:mediaobj.IEnumDMO
title: IEnumDMO (mediaobj.h)
description: The IEnumDMO interface provides methods for enumerating Microsoft DirectX Media Objects (DMOs). It is based on the OLE enumeration interfaces. For more information, see the IEnumXXXX topic in the Platform SDK.
helpviewer_keywords: ["IEnumDMO","IEnumDMO interface [DirectShow]","IEnumDMO interface [DirectShow]","described","IEnumDMOInterface","dshow.ienumdmo","mediaobj/IEnumDMO"]
old-location: dshow\ienumdmo.htm
tech.root: dshow
ms.assetid: 221248f2-5c8f-442e-a6ad-e0372ddc1aae
ms.date: 12/05/2018
ms.keywords: IEnumDMO, IEnumDMO interface [DirectShow], IEnumDMO interface [DirectShow],described, IEnumDMOInterface, dshow.ienumdmo, mediaobj/IEnumDMO
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumDMO
 - mediaobj/IEnumDMO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IEnumDMO
---

# IEnumDMO interface


## -description

The <code>IEnumDMO</code> interface provides methods for enumerating Microsoft DirectX Media Objects (DMOs). It is based on the OLE enumeration interfaces. For more information, see the <i>IEnumXXXX</i> topic in the Platform SDK.



To enumerate registered DMOs, call the <a href="/windows/desktop/api/dmoreg/nf-dmoreg-dmoenum">DMOEnum</a> function.

## -inheritance

The <b>IEnumDMO</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumDMO</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

