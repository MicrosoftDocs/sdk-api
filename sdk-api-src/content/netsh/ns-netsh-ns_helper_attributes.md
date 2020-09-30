---
UID: NS:netsh._NS_HELPER_ATTRIBUTES
title: NS_HELPER_ATTRIBUTES (netsh.h)
description: Provides attributes of a helper.
helpviewer_keywords: ["*PNS_HELPER_ATTRIBUTES","NS_HELPER_ATTRIBUTES","NS_HELPER_ATTRIBUTES structure [NetShell]","PNS_HELPER_ATTRIBUTES","PNS_HELPER_ATTRIBUTES structure pointer [NetShell]","_netsh_ns_helper_attributes","netsh/NS_HELPER_ATTRIBUTES","netsh/PNS_HELPER_ATTRIBUTES","netshell.ns_helper_attributes"]
old-location: netshell\ns_helper_attributes.htm
tech.root: netshell
ms.assetid: b2a3ae40-4aaa-41b2-965c-1467a07ab2de
ms.date: 12/05/2018
ms.keywords: '*PNS_HELPER_ATTRIBUTES, NS_HELPER_ATTRIBUTES, NS_HELPER_ATTRIBUTES structure [NetShell], PNS_HELPER_ATTRIBUTES, PNS_HELPER_ATTRIBUTES structure pointer [NetShell], _netsh_ns_helper_attributes, netsh/NS_HELPER_ATTRIBUTES, netsh/PNS_HELPER_ATTRIBUTES, netshell.ns_helper_attributes'
req.header: netsh.h
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
req.typenames: NS_HELPER_ATTRIBUTES, *PNS_HELPER_ATTRIBUTES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NS_HELPER_ATTRIBUTES
 - netsh/_NS_HELPER_ATTRIBUTES
 - PNS_HELPER_ATTRIBUTES
 - netsh/PNS_HELPER_ATTRIBUTES
 - NS_HELPER_ATTRIBUTES
 - netsh/NS_HELPER_ATTRIBUTES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netsh.h
api_name:
 - NS_HELPER_ATTRIBUTES
---

# NS_HELPER_ATTRIBUTES structure


## -description

The 
<b>NS_HELPER_ATTRIBUTES</b> structure provides attributes of a helper.

## -struct-fields

### -field dwVersion

The version of the helper.

### -field dwReserved

Reserved. Must be zero.

### -field _ullAlign

### -field guidHelper

The GUID of the helper.

### -field pfnStart

A pointer to the 
<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_helper_start_fn">NS_HELPER_START_FN</a> entry point (the start function) of the helper.

### -field pfnStop

A pointer to the 
<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_helper_stop_fn">NS_HELPER_STOP_FN</a> entry point (the stop function) of the helper. Set to null if no stop function is implemented.

## -see-also

<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_helper_start_fn">NS_HELPER_START_FN</a>



<a href="/previous-versions/windows/desktop/api/netsh/nc-netsh-ns_helper_stop_fn">NS_HELPER_STOP_FN</a>