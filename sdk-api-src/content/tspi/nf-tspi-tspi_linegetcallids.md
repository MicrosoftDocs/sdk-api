---
UID: NF:tspi.TSPI_lineGetCallIDs
title: TSPI_lineGetCallIDs function (tspi.h)
description: The TSPI_lineGetCallIDs function returns the call identifiers for the service provider. This function requires TAPI 3.0 version negotiation.
helpviewer_keywords: ["TSPI_lineGetCallIDs","TSPI_lineGetCallIDs function [TAPI 2.2]","_tspi_tspi_linegetcallids","tspi.tspi_linegetcallids","tspi/TSPI_lineGetCallIDs"]
old-location: tspi\tspi_linegetcallids.htm
tech.root: tapi3
ms.assetid: d2a23712-a144-416c-a914-935f1776c256
ms.date: 12/05/2018
ms.keywords: TSPI_lineGetCallIDs, TSPI_lineGetCallIDs function [TAPI 2.2], _tspi_tspi_linegetcallids, tspi.tspi_linegetcallids, tspi/TSPI_lineGetCallIDs
req.header: tspi.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TSPI_lineGetCallIDs
 - tspi/TSPI_lineGetCallIDs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineGetCallIDs
---

# TSPI_lineGetCallIDs function


## -description

The 
<b>TSPI_lineGetCallIDs</b> function returns the call identifiers for the service provider. This function requires TAPI 3.0 version negotiation.

## -parameters

### -param hdCall

The service provider's handle to the call whose identifier is needed.

### -param lpdwAddressID

A pointer to the call's address identifier.

### -param lpdwCallID

A pointer to the call's identifier.

### -param lpdwRelatedCallID

A pointer to the identifier of a related call.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

## -remarks

In some telephony environments, the switch or service provider can assign a unique identifier to each call. This allows the call to be tracked across transfers, forwards, or other events. The domain of these call identifiers and their scope is service-provider defined.

## -see-also

<a href="/windows/desktop/Tapi/callhub-support">CallHub Tracking</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallhubtrackinginfo">LINECALLHUBTRACKINGINFO</a>