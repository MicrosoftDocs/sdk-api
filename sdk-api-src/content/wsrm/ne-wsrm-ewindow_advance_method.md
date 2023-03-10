---
UID: NE:wsrm.eWINDOW_ADVANCE_METHOD
title: eWINDOW_ADVANCE_METHOD (wsrm.h)
description: The eWINDOW_ADVANCE_METHOD enumeration specifies the window advance mode used for Reliable Multicast.
helpviewer_keywords: ["E_WINDOW_ADVANCE_BY_TIME","E_WINDOW_USE_AS_DATA_CACHE","eWINDOW_ADVANCE_METHOD","eWINDOW_ADVANCE_METHOD enumeration [Winsock]","winsock.ewindow_advance_method","wsrm/E_WINDOW_ADVANCE_BY_TIME","wsrm/E_WINDOW_USE_AS_DATA_CACHE","wsrm/eWINDOW_ADVANCE_METHOD"]
old-location: winsock\ewindow_advance_method.htm
tech.root: WinSock
ms.assetid: cd6f0809-ca6b-4a83-ae21-aea1cb4a101a
ms.date: 12/05/2018
ms.keywords: E_WINDOW_ADVANCE_BY_TIME, E_WINDOW_USE_AS_DATA_CACHE, eWINDOW_ADVANCE_METHOD, eWINDOW_ADVANCE_METHOD enumeration [Winsock], winsock.ewindow_advance_method, wsrm/E_WINDOW_ADVANCE_BY_TIME, wsrm/E_WINDOW_USE_AS_DATA_CACHE, wsrm/eWINDOW_ADVANCE_METHOD
req.header: wsrm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - eWINDOW_ADVANCE_METHOD
 - wsrm/eWINDOW_ADVANCE_METHOD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsrm.h
api_name:
 - eWINDOW_ADVANCE_METHOD
---

# eWINDOW_ADVANCE_METHOD enumeration


## -description

The <b>eWINDOW_ADVANCE_METHOD</b> enumeration specifies the window advance mode used  for Reliable Multicast.

## -enum-fields

### -field E_WINDOW_ADVANCE_BY_TIME:1

Window advances based on time. This is the default mode.

### -field E_WINDOW_USE_AS_DATA_CACHE

Use the receive window as a data cache.

## -see-also

<a href="/windows/desktop/WinSock/reliable-multicast-programming--pgm-">Reliable Multicast Programming</a>



<a href="/windows/desktop/WinSock/socket-options">Socket
  Options</a>
