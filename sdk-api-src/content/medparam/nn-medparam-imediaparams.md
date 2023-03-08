---
UID: NN:medparam.IMediaParams
title: IMediaParams (medparam.h)
description: The IMediaParams interface sets and retrieves envelope-following parameters on an object.
helpviewer_keywords: ["IMediaParams","IMediaParams interface [DirectShow]","IMediaParams interface [DirectShow]","described","IMediaParamsInterface","dshow.imediaparams","medparam/IMediaParams"]
old-location: dshow\imediaparams.htm
tech.root: dshow
ms.assetid: 68ea8f6a-4b6d-4d79-a986-6032b767147b
ms.date: 12/05/2018
ms.keywords: IMediaParams, IMediaParams interface [DirectShow], IMediaParams interface [DirectShow],described, IMediaParamsInterface, dshow.imediaparams, medparam/IMediaParams
req.header: medparam.h
req.include-header: 
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
 - IMediaParams
 - medparam/IMediaParams
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
 - IMediaParams
---

# IMediaParams interface


## -description

The <code>IMediaParams</code> interface sets and retrieves envelope-following parameters on an object.



To reduce overhead, parameters are referenced by index value, and all parameter values are 32 bits, defined as type <b>MP_DATA</b>. Use the <a href="/windows/desktop/api/medparam/nn-medparam-imediaparaminfo">IMediaParamInfo</a> interface to determine whether a given parameter is an integer, floating-point value, Boolean value, or member of an enumerated type.

## -inheritance

The <b>IMediaParams</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMediaParams</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

