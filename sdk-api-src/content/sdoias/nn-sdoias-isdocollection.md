---
UID: NN:sdoias.ISdoCollection
title: ISdoCollection (sdoias.h)
description: Use the ISdoCollection interface to manipulate a collection of SDO objects.
helpviewer_keywords: ["ISdoCollection","ISdoCollection interface [Network Policy Server]","ISdoCollection interface [Network Policy Server]","described","_sdo_isdocollection","nps.SDO_isdocollection","sdo.isdocollection","sdoias/ISdoCollection"]
old-location: nps\SDO_isdocollection.htm
tech.root: Nps
ms.assetid: 26470906-1cba-41fc-96f3-078208ab3d51
ms.date: 12/05/2018
ms.keywords: ISdoCollection, ISdoCollection interface [Network Policy Server], ISdoCollection interface [Network Policy Server],described, _sdo_isdocollection, nps.SDO_isdocollection, sdo.isdocollection, sdoias/ISdoCollection
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Iassdo.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISdoCollection
 - sdoias/ISdoCollection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdoCollection
---

# ISdoCollection interface


## -description

Use the 
<b>ISdoCollection</b> interface to manipulate a collection of SDO objects.

## -inheritance

The <b>ISdoCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISdoCollection</b> also has these types of members:

## -remarks

To obtain a collection, call 
<a href="/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty">ISdo::GetProperty</a>, specifying a collection's property. For more information, see 
<a href="/windows/desktop/Nps/sdo-retrieving-a-collection">Retrieving a Collection</a>.

## -see-also

<a href="/windows/desktop/Nps/sdo-collections">Collections</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/Nps/sdo-server-data-objects-interfaces">Server Data Objects Interfaces</a>



<a href="/windows/desktop/Nps/sdo-server-data-objects-reference">Server Data Objects Reference</a>
