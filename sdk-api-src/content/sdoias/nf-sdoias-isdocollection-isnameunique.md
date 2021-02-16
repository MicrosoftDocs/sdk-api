---
UID: NF:sdoias.ISdoCollection.IsNameUnique
title: ISdoCollection::IsNameUnique (sdoias.h)
description: The IsNameUnique method tests whether the specified name is unique in the collection.
helpviewer_keywords: ["ISdoCollection interface [Network Policy Server]","IsNameUnique method","ISdoCollection.IsNameUnique","ISdoCollection::IsNameUnique","IsNameUnique","IsNameUnique method [Network Policy Server]","IsNameUnique method [Network Policy Server]","ISdoCollection interface","_sdo_isdocollection_isnameunique","nps.SDO_isdocollection_isnameunique","sdo.isdocollection_isnameunique","sdoias/ISdoCollection::IsNameUnique"]
old-location: nps\SDO_isdocollection_isnameunique.htm
tech.root: Nps
ms.assetid: cf9263c3-5d98-4b52-bbd7-6a37fb4c8481
ms.date: 12/05/2018
ms.keywords: ISdoCollection interface [Network Policy Server],IsNameUnique method, ISdoCollection.IsNameUnique, ISdoCollection::IsNameUnique, IsNameUnique, IsNameUnique method [Network Policy Server], IsNameUnique method [Network Policy Server],ISdoCollection interface, _sdo_isdocollection_isnameunique, nps.SDO_isdocollection_isnameunique, sdo.isdocollection_isnameunique, sdoias/ISdoCollection::IsNameUnique
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
 - ISdoCollection::IsNameUnique
 - sdoias/ISdoCollection::IsNameUnique
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
 - ISdoCollection.IsNameUnique
---

# ISdoCollection::IsNameUnique


## -description

The 
<b>IsNameUnique</b> method tests whether the specified name is unique in the collection.

## -parameters

### -param bstrName [in]

Specifies the name to test.

### -param pBool [out]

Pointer to a <b>VARIANT</b> that specifies whether the name is unique. The returned value is <b>VARIANT_TRUE</b> if the name is unique, <b>VARIANT_FALSE</b> otherwise.

## -returns

If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

## -remarks

Neither of the parameters may be <b>NULL</b>.

## -see-also

<a href="/windows/desktop/Nps/sdo-adding-an-object-to-a-collection">Adding an Object to a Collection</a>



<a href="/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties">IASCOMMONPROPERTIES</a>



<a href="/windows/desktop/api/sdoias/nn-sdoias-isdocollection">ISdoCollection</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdocollection-add">ISdoCollection::Add</a>



<a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a>