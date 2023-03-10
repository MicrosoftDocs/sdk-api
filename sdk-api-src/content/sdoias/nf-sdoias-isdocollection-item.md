---
UID: NF:sdoias.ISdoCollection.Item
title: ISdoCollection::Item (sdoias.h)
description: The Item method retrieves the specified item from the collection.
helpviewer_keywords: ["ISdoCollection interface [Network Policy Server]","Item method","ISdoCollection.Item","ISdoCollection::Item","Item","Item method [Network Policy Server]","Item method [Network Policy Server]","ISdoCollection interface","_sdo_isdocollection_item","nps.SDO_isdocollection_item","sdo.isdocollection_item","sdoias/ISdoCollection::Item"]
old-location: nps\SDO_isdocollection_item.htm
tech.root: Nps
ms.assetid: 1c830e23-dc6f-49dd-83fe-8ddd39ac1bf6
ms.date: 12/05/2018
ms.keywords: ISdoCollection interface [Network Policy Server],Item method, ISdoCollection.Item, ISdoCollection::Item, Item, Item method [Network Policy Server], Item method [Network Policy Server],ISdoCollection interface, _sdo_isdocollection_item, nps.SDO_isdocollection_item, sdo.isdocollection_item, sdoias/ISdoCollection::Item
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
 - ISdoCollection::Item
 - sdoias/ISdoCollection::Item
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
 - ISdoCollection.Item
---

# ISdoCollection::Item


## -description

The 
<b>Item</b> method retrieves the specified item from the collection.

## -parameters

### -param Name [in]

Pointer to a 
<a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a>. Store the name of the object in a 
<a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a> in this <b>VARIANT</b>.

### -param pItem [out]

Pointer to an interface pointer that receives the address of an 
<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface for the object.

## -returns

If the method succeeds the return value is <b>S_OK</b>.

If the object is not found in the collection, the return value is <b>DISP_E_MEMBERNOTFOUND</b>.

Otherwise, if the method fails, the return value is one of the following error codes.

## -remarks

Neither of the parameters can be <b>NULL</b>.

## -see-also

<a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a>



<a href="/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties">IASCOMMONPROPERTIES</a>



<a href="/windows/desktop/api/sdoias/nn-sdoias-isdocollection">ISdoCollection</a>



<a href="/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection">Retrieving an Object from a Collection</a>



<a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a>