---
UID: NN:strmif.IPinConnection
title: IPinConnection (strmif.h)
description: This interface provides methods for reconnecting an input pin while the filter is still running.
helpviewer_keywords: ["IPinConnection","IPinConnection interface [DirectShow]","IPinConnection interface [DirectShow]","described","IPinConnectionInterface","dshow.ipinconnection","strmif/IPinConnection"]
old-location: dshow\ipinconnection.htm
tech.root: dshow
ms.assetid: 0843a01c-6f6a-4765-abca-dd562175fcee
ms.date: 12/05/2018
ms.keywords: IPinConnection, IPinConnection interface [DirectShow], IPinConnection interface [DirectShow],described, IPinConnectionInterface, dshow.ipinconnection, strmif/IPinConnection
req.header: strmif.h
req.include-header: Dshow.h
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
 - IPinConnection
 - strmif/IPinConnection
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
 - IPinConnection
---

# IPinConnection interface


## -description

This interface provides methods for reconnecting an input pin while the filter is still running. The Filter Graph Manager calls methods on this interface when it performs dynamic reconnections (see the <a href="/windows/desktop/api/strmif/nn-strmif-igraphconfig">IGraphConfig</a> interface). Applications might also use this interface to perform dynamic pin reconnections.

<b>Filter developers: </b>Implement this interface on any input pin that allows dynamic reconnection or dynamic changes in format.

## -inheritance

The <b>IPinConnection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPinConnection</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/dynamic-graph-building">Dynamic Graph Building</a>



<a href="/windows/desktop/DirectShow/dynamic-reconnection">Dynamic Reconnection</a>
