---
UID: NF:comsvcs.IComTrackingInfoCollection.Type
title: IComTrackingInfoCollection::Type (comsvcs.h)
description: Retrieves the type of a tracking information collection.
helpviewer_keywords: ["IComTrackingInfoCollection interface [COM+]","Type method","IComTrackingInfoCollection.Type","IComTrackingInfoCollection::Type","Type","Type method [COM+]","Type method [COM+]","IComTrackingInfoCollection interface","_dtc_IComTrackingInfoCollection_Type","comsvcs/IComTrackingInfoCollection::Type","cos.icomtrackinginfocollection_type"]
old-location: cos\icomtrackinginfocollection_type.htm
tech.root: cos
ms.assetid: ee7c16ac-be47-44e7-b8a6-46a7ec29a2c1
ms.date: 12/05/2018
ms.keywords: IComTrackingInfoCollection interface [COM+],Type method, IComTrackingInfoCollection.Type, IComTrackingInfoCollection::Type, Type, Type method [COM+], Type method [COM+],IComTrackingInfoCollection interface, _dtc_IComTrackingInfoCollection_Type, comsvcs/IComTrackingInfoCollection::Type, cos.icomtrackinginfocollection_type
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IComTrackingInfoCollection::Type
 - comsvcs/IComTrackingInfoCollection::Type
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComTrackingInfoCollection.Type
---

# IComTrackingInfoCollection::Type


## -description

Retrieves the type of a tracking information collection.

## -parameters

### -param pType [out]

The type of tracking information. For a list of values, see the <a href="/windows/win32/api/comsvcs/ne-comsvcs-tracking_coll_type">TRACKING_COLL_TYPE</a> enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomtrackinginfocollection">IComTrackingInfoCollection</a>