---
UID: NF:bdaiface.IMPEG2PIDMap.EnumPIDMap
title: IMPEG2PIDMap::EnumPIDMap (bdaiface.h)
description: The EnumPIDMap method returns a collection of all the currently mapped PIDs on this pin.
helpviewer_keywords: ["EnumPIDMap","EnumPIDMap method [DirectShow]","EnumPIDMap method [DirectShow]","IMPEG2PIDMap interface","IMPEG2PIDMap interface [DirectShow]","EnumPIDMap method","IMPEG2PIDMap.EnumPIDMap","IMPEG2PIDMap::EnumPIDMap","IMPEG2PIDMapEnumPIDMap","bdaiface/IMPEG2PIDMap::EnumPIDMap","dshow.impeg2pidmap_enumpidmap"]
old-location: dshow\impeg2pidmap_enumpidmap.htm
tech.root: dshow
ms.assetid: 9e5dbc92-e072-4e59-b7b2-07ae39cb9d59
ms.date: 12/05/2018
ms.keywords: EnumPIDMap, EnumPIDMap method [DirectShow], EnumPIDMap method [DirectShow],IMPEG2PIDMap interface, IMPEG2PIDMap interface [DirectShow],EnumPIDMap method, IMPEG2PIDMap.EnumPIDMap, IMPEG2PIDMap::EnumPIDMap, IMPEG2PIDMapEnumPIDMap, bdaiface/IMPEG2PIDMap::EnumPIDMap, dshow.impeg2pidmap_enumpidmap
req.header: bdaiface.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMPEG2PIDMap::EnumPIDMap
 - bdaiface/IMPEG2PIDMap::EnumPIDMap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMPEG2PIDMap.EnumPIDMap
---

# IMPEG2PIDMap::EnumPIDMap


## -description

The <code>EnumPIDMap</code> method returns a collection of all the currently mapped PIDs on this pin.

## -parameters

### -param pIEnumPIDMap [in]

Receives an <a href="/windows/desktop/api/bdaiface/nn-bdaiface-ienumpidmap">IEnumPIDMap</a> pointer. Use this interface to enumerate the mapped PIDs. The caller must release the interface.

## -returns

Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/bdaiface/nn-bdaiface-impeg2pidmap">IMPEG2PIDMap Interface</a>