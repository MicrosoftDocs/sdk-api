---
UID: NF:tspi.TSPI_lineSetCallHubTracking
title: TSPI_lineSetCallHubTracking function (tspi.h)
author: windows-sdk-content
description: The TSPI_lineSetCallHubTracking function sets the CallHub tracking mode. This function requires TAPI 3.0 version negotiation.
old-location: tspi\tspi_linesetcallhubtracking.htm
tech.root: Tapi
ms.assetid: ec2d5d46-1c83-47a0-9c10-684959630a16
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TSPI_lineSetCallHubTracking, TSPI_lineSetCallHubTracking function [TAPI 2.2], _tspi_tspi_linesetcallhubtracking, tspi.tspi_linesetcallhubtracking, tspi/TSPI_lineSetCallHubTracking
ms.topic: function
f1_keywords: 
 - "tspi/TSPI_lineSetCallHubTracking"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineSetCallHubTracking
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TSPI_lineSetCallHubTracking function


## -description


The 
<b>TSPI_lineSetCallHubTracking</b> function sets the CallHub tracking mode. This function requires TAPI 3.0 version negotiation.


## -parameters




### -param hdLine

The service provider's handle to the call whose call information is to be retrieved. The call state of <i>hdCall</i> can be any state.


### -param lpTrackingInfo

A pointer to a variably sized structure of type 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linecallhubtrackinginfo">LINECALLHUBTRACKINGINFO</a>. Upon successful completion of the request, this structure is filled with call-related information.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/callhub-object">CallHub Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linecallhubtrackinginfo">LINECALLHUBTRACKINGINFO</a>
 

 

