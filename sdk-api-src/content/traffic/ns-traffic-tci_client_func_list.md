---
UID: NS:traffic._TCI_CLIENT_FUNC_LIST
title: TCI_CLIENT_FUNC_LIST (traffic.h)
description: The TCI_CLIENT_FUNC_LIST structure is used by the traffic control interface to register and then access client callback functions. Each member of TCI_CLIENT_FUNC_LIST is a pointer to the client-provided callback function.
helpviewer_keywords: ["*PTCI_CLIENT_FUNC_LIST","PTCI_CLIENT_FUNC_LIST","PTCI_CLIENT_FUNC_LIST structure pointer [QOS]","TCI_CLIENT_FUNC_LIST","TCI_CLIENT_FUNC_LIST structure [QOS]","_gqos_tci_client_func_list","qos.tci_client_func_list","traffic/PTCI_CLIENT_FUNC_LIST","traffic/TCI_CLIENT_FUNC_LIST"]
old-location: qos\tci_client_func_list.htm
tech.root: QOS
ms.assetid: 45eccc44-d170-49cc-b51d-bb502c2fc1c7
ms.date: 12/05/2018
ms.keywords: '*PTCI_CLIENT_FUNC_LIST, PTCI_CLIENT_FUNC_LIST, PTCI_CLIENT_FUNC_LIST structure pointer [QOS], TCI_CLIENT_FUNC_LIST, TCI_CLIENT_FUNC_LIST structure [QOS], _gqos_tci_client_func_list, qos.tci_client_func_list, traffic/PTCI_CLIENT_FUNC_LIST, traffic/TCI_CLIENT_FUNC_LIST'
req.header: traffic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: TCI_CLIENT_FUNC_LIST, *PTCI_CLIENT_FUNC_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TCI_CLIENT_FUNC_LIST
 - traffic/_TCI_CLIENT_FUNC_LIST
 - PTCI_CLIENT_FUNC_LIST
 - traffic/PTCI_CLIENT_FUNC_LIST
 - TCI_CLIENT_FUNC_LIST
 - traffic/TCI_CLIENT_FUNC_LIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Traffic.h
api_name:
 - TCI_CLIENT_FUNC_LIST
---

# TCI_CLIENT_FUNC_LIST structure


## -description

The 
<b>TCI_CLIENT_FUNC_LIST</b> structure is used by the traffic control interface to register and then access client-callback functions. Each member of 
<b>TCI_CLIENT_FUNC_LIST</b> is a pointer to the client provided–callback function.

## -struct-fields

### -field ClNotifyHandler

Pointer to the client-callback function 
<a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_notify_handler">ClNotifyHandler</a>.

### -field ClAddFlowCompleteHandler

Pointer to the client-callback function <a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_add_flow_complete_handler">ClAddFlowComplete</a>.

### -field ClModifyFlowCompleteHandler

Pointer to the client-callback function <a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_mod_flow_complete_handler">ClModifyFlowComplete</a>.

### -field ClDeleteFlowCompleteHandler

Pointer to the client-callback function <a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_del_flow_complete_handler">ClDeleteFlowComplete</a>.

## -remarks

Any member of the 
<b>TCI_CLIENT_FUNC_LIST</b> structure can be <b>NULL</b> except <b>ClNotifyHandler</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_add_flow_complete_handler">ClAddFlowComplete</a>



<a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_del_flow_complete_handler">ClDeleteFlowComplete</a>



<a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_mod_flow_complete_handler">ClModifyFlowComplete</a>



<a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_notify_handler">ClNotifyHandler</a>
