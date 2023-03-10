---
UID: NF:sdoias.ISdoCollection.get_Count
title: ISdoCollection::get_Count (sdoias.h)
description: The get_Count method returns the number of items in the collection.
helpviewer_keywords: ["ISdoCollection interface [Network Policy Server]","get_Count method","ISdoCollection.get_Count","ISdoCollection::get_Count","_sdo_isdocollection_get_count","get_Count","get_Count method [Network Policy Server]","get_Count method [Network Policy Server]","ISdoCollection interface","nps.SDO_isdocollection_get_count","sdo.isdocollection_get_count","sdoias/ISdoCollection::get_Count"]
old-location: nps\SDO_isdocollection_get_count.htm
tech.root: Nps
ms.assetid: 57f83f72-327b-4018-be1b-3527820f88d5
ms.date: 12/05/2018
ms.keywords: ISdoCollection interface [Network Policy Server],get_Count method, ISdoCollection.get_Count, ISdoCollection::get_Count, _sdo_isdocollection_get_count, get_Count, get_Count method [Network Policy Server], get_Count method [Network Policy Server],ISdoCollection interface, nps.SDO_isdocollection_get_count, sdo.isdocollection_get_count, sdoias/ISdoCollection::get_Count
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
 - ISdoCollection::get_Count
 - sdoias/ISdoCollection::get_Count
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
 - ISdoCollection.get_Count
---

# ISdoCollection::get_Count


## -description

The 
<b>get_Count</b> method returns the number of items in the collection.

## -parameters

### -param pCount [out]

Pointer to a <b>LONG</b> that contains the number of items in the collection.

## -returns

If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.

## -see-also

<a href="/windows/desktop/api/sdoias/nn-sdoias-isdocollection">ISdoCollection</a>



<a href="/windows/desktop/api/sdoias/nf-sdoias-isdocollection-get__newenum">ISdoCollection::get__NewEnum</a>