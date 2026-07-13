---
UID: NN:bits3_0.IBitsPeerCacheAdministration
title: IBitsPeerCacheAdministration (bits3_0.h)
description: Use IBitsPeerCacheAdministration to manage the pool of peers from which you can download content.
helpviewer_keywords: ["IBitsPeerCacheAdministration","IBitsPeerCacheAdministration interface [BITS]","IBitsPeerCacheAdministration interface [BITS]","described","bits.ibitspeercacheadministration","bits3_0/IBitsPeerCacheAdministration"]
old-location: bits\ibitspeercacheadministration.htm
tech.root: Bits
ms.assetid: 5fa30b4e-f13c-4341-af65-a2e3d2703b96
ms.date: 12/05/2018
ms.keywords: IBitsPeerCacheAdministration, IBitsPeerCacheAdministration interface [BITS], IBitsPeerCacheAdministration interface [BITS],described, bits.ibitspeercacheadministration, bits3_0/IBitsPeerCacheAdministration
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBitsPeerCacheAdministration
 - bits3_0/IBitsPeerCacheAdministration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBitsPeerCacheAdministration
---

# IBitsPeerCacheAdministration interface


## -description

Use <b>IBitsPeerCacheAdministration</b> to manage the pool of peers from which you can download content. 

To get this interface, call the <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager">IBackgroundCopyManager::QueryInterface</a> method, using __uuidof(IBitsPeerCacheAdministration) as the interface identifier. 
<div class="alert"><b>Note</b>  This interface is deprecated in BITS 4.0, and all of the API methods will return <b>S_FALSE</b>.</div><div> </div>

## -inheritance

The <b>IBitsPeerCacheAdministration</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBitsPeerCacheAdministration</b> also has these types of members:

## -remarks

 You should never have to manage the peer cache; BITS manages the cache for you.

You must have administrator privileges to modify the cache.

## -see-also

<a href="/windows/desktop/Bits/administering-the-peer-cache">Administering the Peer Cache</a>



<a href="/windows/desktop/Bits/peer-caching">Peer Caching</a>
