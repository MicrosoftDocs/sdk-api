---
UID: NF:sdoias.ISdoCollection.Remove
title: ISdoCollection::Remove (sdoias.h)
description: The Remove method removes the specified item from the collection.
helpviewer_keywords: ["ISdoCollection interface [Network Policy Server]","Remove method","ISdoCollection.Remove","ISdoCollection::Remove","Remove","Remove method [Network Policy Server]","Remove method [Network Policy Server]","ISdoCollection interface","_sdo_isdocollection_remove","nps.SDO_isdocollection_remove","sdo.isdocollection_remove","sdoias/ISdoCollection::Remove"]
old-location: nps\SDO_isdocollection_remove.htm
tech.root: Nps
ms.assetid: f390377d-b78e-4548-9602-c0eb363765c7
ms.date: 12/05/2018
ms.keywords: ISdoCollection interface [Network Policy Server],Remove method, ISdoCollection.Remove, ISdoCollection::Remove, Remove, Remove method [Network Policy Server], Remove method [Network Policy Server],ISdoCollection interface, _sdo_isdocollection_remove, nps.SDO_isdocollection_remove, sdo.isdocollection_remove, sdoias/ISdoCollection::Remove
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
 - ISdoCollection::Remove
 - sdoias/ISdoCollection::Remove
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
 - ISdoCollection.Remove
---

# ISdoCollection::Remove


## -description

The 
<b>Remove</b> method removes the specified item from the collection.

## -parameters

### -param pItem [in]

Pointer to an 
<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface that specifies the item to remove.

This parameter must not be <b>NULL</b>.

## -returns

If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

## -see-also

<a href="/windows/desktop/api/sdoias/nn-sdoias-isdocollection">ISdoCollection</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdocollection-add">ISdoCollection::Add</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdocollection-removeall">ISdoCollection::RemoveAll</a>