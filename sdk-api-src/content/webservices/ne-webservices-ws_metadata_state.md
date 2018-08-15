---
UID: NE:webservices.WS_METADATA_STATE
title: WS_METADATA_STATE
author: windows-sdk-content
description: The state of the metadata object.
old-location: wsw\ws_metadata_state.htm
old-project: wsw
ms.assetid: 4d2b8c31-d5ff-4b96-9aaf-57e59d075431
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WS_METADATA_STATE, WS_METADATA_STATE enumeration [Web Services for Windows], WS_METADATA_STATE_CREATED, WS_METADATA_STATE_FAULTED, WS_METADATA_STATE_RESOLVED, webservices/WS_METADATA_STATE, webservices/WS_METADATA_STATE_CREATED, webservices/WS_METADATA_STATE_FAULTED, webservices/WS_METADATA_STATE_RESOLVED, wsw.ws_metadata_state
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WS_METADATA_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_METADATA_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_METADATA_STATE enumeration


## -description


The state of the metadata object.
            


## -enum-fields




### -field WS_METADATA_STATE_CREATED

The initial state of the metadata object.
                


### -field WS_METADATA_STATE_RESOLVED

All references between metadata documents have been
                    resolved and no more metadata documents may be added
                    to the metadata object.  See <a href="https://msdn.microsoft.com/1cf9f2ba-c303-4668-a959-8fad69746438">WsGetMetadataEndpoints</a> for
                    more information.
                


### -field WS_METADATA_STATE_FAULTED

The metadata object not usable due to a previous error.  See
                    See <a href="https://msdn.microsoft.com/1cf9f2ba-c303-4668-a959-8fad69746438">WsGetMetadataEndpoints</a> and <a href="https://msdn.microsoft.com/0b824948-e06d-482d-8d53-c4e27d1ecf0f">WsReadMetadata</a>for more information.
                


## -remarks



The following diagram illustrates the functions that 
                cause state transitions in the metadata object.
            

<img alt="" src="./images/MetadataStates.png"/>



