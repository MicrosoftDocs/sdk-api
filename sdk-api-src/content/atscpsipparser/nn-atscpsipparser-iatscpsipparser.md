---
UID: NN:atscpsipparser.IAtscPsipParser
title: IAtscPsipParser (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later. The IAtscPsipParser interface retrieves ATSC Program and System Information Protocol (PSIP) tables.
helpviewer_keywords: ["IAtscPsipParser","IAtscPsipParser interface [Microsoft TV Technologies]","IAtscPsipParser interface [Microsoft TV Technologies]","described","IAtscPsipParserInterface","atscpsipparser/IAtscPsipParser","mstv.iatscpsipparser"]
old-location: mstv\iatscpsipparser.htm
tech.root: mstv
ms.assetid: dbe922b3-b843-4eaa-807d-5608cfbb9686
ms.date: 12/05/2018
ms.keywords: IAtscPsipParser, IAtscPsipParser interface [Microsoft TV Technologies], IAtscPsipParser interface [Microsoft TV Technologies],described, IAtscPsipParserInterface, atscpsipparser/IAtscPsipParser, mstv.iatscpsipparser
req.header: atscpsipparser.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAtscPsipParser
 - atscpsipparser/IAtscPsipParser
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IAtscPsipParser
---

# IAtscPsipParser interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IAtscPsipParser</b> interface retrieves ATSC Program and System Information Protocol (PSIP) tables.

## -inheritance

The <b>IAtscPsipParser</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAtscPsipParser</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To get a pointer to this interface, call <b>CoCreateInstance</b>. Use the following CLSID:


```cpp
3508C064-B94E-420b-A821-20C8096FAADC
```


This CLSID is not is not published in an SDK header; define a new GUID constant in your application.

You must call <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-initialize">Initialize</a> before calling any other methods on the object.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
