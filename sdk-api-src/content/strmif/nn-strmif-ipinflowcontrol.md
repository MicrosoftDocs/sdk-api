---
UID: NN:strmif.IPinFlowControl
title: IPinFlowControl (strmif.h)
description: Blocks data flow from an active output pin.
helpviewer_keywords: ["IPinFlowControl","IPinFlowControl interface [DirectShow]","IPinFlowControl interface [DirectShow]","described","IPinFlowControlInterface","dshow.ipinflowcontrol","strmif/IPinFlowControl"]
old-location: dshow\ipinflowcontrol.htm
tech.root: dshow
ms.assetid: 27e607d9-85f0-4e17-b8e7-6df729288acd
ms.date: 12/05/2018
ms.keywords: IPinFlowControl, IPinFlowControl interface [DirectShow], IPinFlowControl interface [DirectShow],described, IPinFlowControlInterface, dshow.ipinflowcontrol, strmif/IPinFlowControl
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
 - IPinFlowControl
 - strmif/IPinFlowControl
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
 - IPinFlowControl
---

# IPinFlowControl interface


## -description

Blocks data flow from an active output pin. This interface is exposed by output pins that can reconnect dynamically. Use this interface to start a dynamic reconnection within the filter graph. For more information, see <a href="/windows/desktop/DirectShow/dynamic-graph-building">Dynamic Graph Building</a>.

<b>Filter developers: </b>Parser and capture filters that support dynamic reconnection should support this interface on their output pins. Generally, other types of filters do not need to implement this interface.

## -inheritance

The <b>IPinFlowControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPinFlowControl</b> also has these types of members:

