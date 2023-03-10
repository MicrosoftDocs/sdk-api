---
UID: NF:sdoias.ISdoCollection.Add
title: ISdoCollection::Add (sdoias.h)
description: The Add method adds an item to the Server Data Objects (SDO) collection.
helpviewer_keywords: ["Add","Add method [Network Policy Server]","Add method [Network Policy Server]","ISdoCollection interface","ISdoCollection interface [Network Policy Server]","Add method","ISdoCollection.Add","ISdoCollection::Add","_sdo_isdocollection_add","nps.SDO_isdocollection_add","sdo.isdocollection_add","sdoias/ISdoCollection::Add"]
old-location: nps\SDO_isdocollection_add.htm
tech.root: Nps
ms.assetid: a575b224-9827-47f3-a819-bd793200c901
ms.date: 12/05/2018
ms.keywords: Add, Add method [Network Policy Server], Add method [Network Policy Server],ISdoCollection interface, ISdoCollection interface [Network Policy Server],Add method, ISdoCollection.Add, ISdoCollection::Add, _sdo_isdocollection_add, nps.SDO_isdocollection_add, sdo.isdocollection_add, sdoias/ISdoCollection::Add
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
 - ISdoCollection::Add
 - sdoias/ISdoCollection::Add
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
 - ISdoCollection.Add
---

# ISdoCollection::Add


## -description

The 
<b>Add</b> method adds an item to the Server Data Objects (SDO) collection.

## -parameters

### -param bstrName [in]

Specifies the name of the SDO Object. This parameter may be <b>NULL</b>.

### -param ppItem [in, out]

Pointer to an <b>IDispatch</b> interface pointer for the Item to add. This parameter must not be <b>NULL</b>.

## -returns

If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

## -remarks

If you specify the name of the object to add, ensure that the name is unique by calling 
<a href="/windows/desktop/api/sdoias/nf-sdoias-isdocollection-isnameunique">ISdoCollection::IsNameUnique</a>.

If the <i>bstrName</i> parameter is not specified, <b>ISdoCollection::Add</b> obtains it from the object specified by the <i>ppItem</i> parameter.

## -see-also

<a href="/windows/desktop/Nps/sdo-adding-an-object-to-a-collection">Adding an Object to a Collection</a>



<a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a>



<a href="/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties">IASCOMMONPROPERTIES</a>



<a href="/windows/desktop/api/sdoias/nn-sdoias-isdocollection">ISdoCollection</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdocollection-isnameunique">ISdoCollection::IsNameUnique</a>