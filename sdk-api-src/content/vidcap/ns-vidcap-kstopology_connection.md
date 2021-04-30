---
UID: NS:vidcap.__MIDL___MIDL_itf_vidcap_0000_0000_0001
title: KSTOPOLOGY_CONNECTION (vidcap.h)
description: This topic applies to Windows XP Service Pack 2 or later. The KSTOPOLOGY_CONNECTION structure describes a node connection within a kernel-streaming (KS) filter. A node can be connected to another node within the filter, or to a pin on the filter.
helpviewer_keywords: ["*PKSTOPOLOGY_CONNECTION","KSTOPOLOGY_CONNECTION","KSTOPOLOGY_CONNECTION structure [DirectShow]","KSTOPOLOGY_CONNECTIONStructure","PKSTOPOLOGY_CONNECTION","PKSTOPOLOGY_CONNECTION structure pointer [DirectShow]","dshow.kstopology_connection","vidcap/KSTOPOLOGY_CONNECTION","vidcap/PKSTOPOLOGY_CONNECTION"]
old-location: dshow\kstopology_connection.htm
tech.root: dshow
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
ms.date: 12/05/2018
ms.keywords: '*PKSTOPOLOGY_CONNECTION, KSTOPOLOGY_CONNECTION, KSTOPOLOGY_CONNECTION structure [DirectShow], KSTOPOLOGY_CONNECTIONStructure, PKSTOPOLOGY_CONNECTION, PKSTOPOLOGY_CONNECTION structure pointer [DirectShow], dshow.kstopology_connection, vidcap/KSTOPOLOGY_CONNECTION, vidcap/PKSTOPOLOGY_CONNECTION'
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: KSTOPOLOGY_CONNECTION, *PKSTOPOLOGY_CONNECTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_vidcap_0000_0000_0001
 - vidcap/__MIDL___MIDL_itf_vidcap_0000_0000_0001
 - PKSTOPOLOGY_CONNECTION
 - vidcap/PKSTOPOLOGY_CONNECTION
 - KSTOPOLOGY_CONNECTION
 - vidcap/KSTOPOLOGY_CONNECTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - vidcap.h
api_name:
 - KSTOPOLOGY_CONNECTION
---

# KSTOPOLOGY_CONNECTION structure


## -description

This topic applies to Windows XP Service Pack 2 or later.
          

The <b>KSTOPOLOGY_CONNECTION</b> structure describes a node connection within a kernel-streaming (KS) filter. A node can be connected to another node within the filter, or to a pin on the filter.

## -struct-fields

### -field FromNode

Index of the upstream node in the connection. If the upstream connection is a pin, rather than a node, the value is KSFILTER_NODE.

### -field FromNodePin

If the value of the <b>FromNode</b> field is KSFILTER_NODE, this field specifies the index of the upstream pin. Otherwise, this field is ignored.

### -field ToNode

Index of the downstream node in the connection. If the downstream connection is a pin, rather than a node, the value is KSFILTER_NODE.

### -field ToNodePin

If the value of the <b>ToNode</b> field is KSFILTER_NODE, this field specifies the index of the downstream pin. Otherwise, this field is ignored.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/api/vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo">IKsTopologyInfo::get_ConnectionInfo</a>