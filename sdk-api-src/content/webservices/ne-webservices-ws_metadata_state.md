---
UID: NE:webservices.__unnamed_enum_103
title: WS_METADATA_STATE (webservices.h)
description: The state of the metadata object.
helpviewer_keywords: ["WS_METADATA_STATE","WS_METADATA_STATE enumeration [Web Services for Windows]","WS_METADATA_STATE_CREATED","WS_METADATA_STATE_FAULTED","WS_METADATA_STATE_RESOLVED","webservices/WS_METADATA_STATE","webservices/WS_METADATA_STATE_CREATED","webservices/WS_METADATA_STATE_FAULTED","webservices/WS_METADATA_STATE_RESOLVED","wsw.ws_metadata_state"]
old-location: wsw\ws_metadata_state.htm
tech.root: wsw
ms.assetid: 4d2b8c31-d5ff-4b96-9aaf-57e59d075431
ms.date: 12/05/2018
ms.keywords: WS_METADATA_STATE, WS_METADATA_STATE enumeration [Web Services for Windows], WS_METADATA_STATE_CREATED, WS_METADATA_STATE_FAULTED, WS_METADATA_STATE_RESOLVED, webservices/WS_METADATA_STATE, webservices/WS_METADATA_STATE_CREATED, webservices/WS_METADATA_STATE_FAULTED, webservices/WS_METADATA_STATE_RESOLVED, wsw.ws_metadata_state
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WS_METADATA_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_METADATA_STATE
 - webservices/WS_METADATA_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_METADATA_STATE
---

# WS_METADATA_STATE enumeration


## -description

The state of the metadata object.

## -enum-fields

### -field WS_METADATA_STATE_CREATED:1

The initial state of the metadata object.

### -field WS_METADATA_STATE_RESOLVED:2

All references between metadata documents have been
                    resolved and no more metadata documents may be added
                    to the metadata object.  See <a href="/windows/desktop/api/webservices/nf-webservices-wsgetmetadataendpoints">WsGetMetadataEndpoints</a> for
                    more information.

### -field WS_METADATA_STATE_FAULTED:3

The metadata object not usable due to a previous error.  See
                    See <a href="/windows/desktop/api/webservices/nf-webservices-wsgetmetadataendpoints">WsGetMetadataEndpoints</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wsreadmetadata">WsReadMetadata</a> for more information.

## -remarks

The following diagram illustrates the functions that 
                cause state transitions in the metadata object.
            
:::image type="content" source="./images/MetadataStates.png" border="false" alt-text="Diagram of the state transitions for a Metadata object showing the functions that cause transitions between the Created, Faulted, and Resolved states.":::
