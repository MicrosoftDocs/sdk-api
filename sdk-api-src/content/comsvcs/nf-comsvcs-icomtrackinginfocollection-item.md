---
UID: NF:comsvcs.IComTrackingInfoCollection.Item
title: IComTrackingInfoCollection::Item (comsvcs.h)
description: Retrieves the specified interface from a specified member of a tracking information collection.
old-location: cos\icomtrackinginfocollection_item.htm
tech.root: cossdk
ms.assetid: 61da742b-d8cd-48db-a9b7-c754b8963907
ms.date: 12/05/2018
ms.keywords: IComTrackingInfoCollection interface [COM+],Item method, IComTrackingInfoCollection.Item, IComTrackingInfoCollection::Item, Item, Item method [COM+], Item method [COM+],IComTrackingInfoCollection interface, _dtc_IComTrackingInfoCollection_Item, comsvcs/IComTrackingInfoCollection::Item, cos.icomtrackinginfocollection_item
ms.topic: method
f1_keywords:
- comsvcs/IComTrackingInfoCollection.Item
dev_langs:
- c++
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ComSvcs.h
api_name:
- IComTrackingInfoCollection.Item
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComTrackingInfoCollection::Item


## -description


Retrieves the specified interface from a specified member of a tracking information collection.


## -parameters




### -param ulIndex [in]

The index of the object in the collection.


### -param riid [in]

The identifier of the interface to be requested.


### -param ppv [out]

A pointer to the requested interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icomtrackinginfocollection">IComTrackingInfoCollection</a>
 

 

