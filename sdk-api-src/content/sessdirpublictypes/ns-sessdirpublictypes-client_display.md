---
UID: NS:sessdirpublictypes.__MIDL___MIDL_itf_sessdirpublictypes_0000_0000_0001
title: CLIENT_DISPLAY (sessdirpublictypes.h)
description: Contains information about the display of a Remote Desktop Connection (RDC) client. (CLIENT_DISPLAY)
helpviewer_keywords: ["*PCLIENT_DISPLAY","CLIENT_DISPLAY","CLIENT_DISPLAY structure [Remote Desktop Services]","PCLIENT_DISPLAY","PCLIENT_DISPLAY structure pointer [Remote Desktop Services]","sessdirpublictypes/CLIENT_DISPLAY","sessdirpublictypes/PCLIENT_DISPLAY","termserv.client_display"]
old-location: termserv\client_display.htm
tech.root: TermServ
ms.assetid: 6436c049-d710-4208-882a-0c7e83b4a079
ms.date: 12/05/2018
ms.keywords: '*PCLIENT_DISPLAY, CLIENT_DISPLAY, CLIENT_DISPLAY structure [Remote Desktop Services], PCLIENT_DISPLAY, PCLIENT_DISPLAY structure pointer [Remote Desktop Services], sessdirpublictypes/CLIENT_DISPLAY, sessdirpublictypes/PCLIENT_DISPLAY, termserv.client_display'
req.header: sessdirpublictypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SessDirPublicTypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CLIENT_DISPLAY, *PCLIENT_DISPLAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_sessdirpublictypes_0000_0000_0001
 - sessdirpublictypes/__MIDL___MIDL_itf_sessdirpublictypes_0000_0000_0001
 - PCLIENT_DISPLAY
 - sessdirpublictypes/PCLIENT_DISPLAY
 - CLIENT_DISPLAY
 - sessdirpublictypes/CLIENT_DISPLAY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - SessDirPublicTypes.h
api_name:
 - CLIENT_DISPLAY
---

# CLIENT_DISPLAY structure


## -description

Contains information about the display of a Remote Desktop Connection (RDC) client.

## -struct-fields

### -field HorizontalResolution

The horizontal dimension, in pixels, of the client's display.

### -field VerticalResolution

The vertical dimension, in pixels, of the client's display.

### -field ColorDepth

The color depth of the client's display. For possible values, see the <b>ColorDepth</b> member of the <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wts_client_display">WTS_CLIENT_DISPLAY</a> structure.
