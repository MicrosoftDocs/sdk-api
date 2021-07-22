---
UID: NN:tapi3if.ITCollection
title: ITCollection (tapi3if.h)
description: The ITCollection interface allows Automation client applications, such as those written in Visual Basic, to retrieve collection information.
helpviewer_keywords: ["ITCollection","ITCollection interface [TAPI 2.2]","ITCollection interface [TAPI 2.2]","described","_tapi3_itcollection","tapi3.itcollection","tapi3if/ITCollection"]
old-location: tapi3\itcollection.htm
tech.root: tapi3
ms.assetid: 2286678a-68b9-4f4a-b36b-7fdf8cdad6a6
ms.date: 12/05/2018
ms.keywords: ITCollection, ITCollection interface [TAPI 2.2], ITCollection interface [TAPI 2.2],described, _tapi3_itcollection, tapi3.itcollection, tapi3if/ITCollection
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITCollection
 - tapi3if/ITCollection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITCollection
---

# ITCollection interface


## -description

The 
<b>ITCollection</b> interface allows Automation client applications, such as those written in Visual Basic, to retrieve collection information. C or C++ programs use enumerator interfaces to retrieve the same information. Collection methods return a <b>VARIANT</b> which contains a pointer to an 
<b>ITCollection</b> interface.

The 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection2">ITCollection2</a> interface is an extension of the 
<b>ITCollection</b> interface. 
<b>ITCollection2</b> exposes additional methods for modifying the collection.

## -inheritance

The <b>ITCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITCollection</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection2">ITCollection2</a>
