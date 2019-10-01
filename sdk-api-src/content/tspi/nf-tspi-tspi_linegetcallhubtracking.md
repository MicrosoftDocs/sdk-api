---
UID: NF:tspi.TSPI_lineGetCallHubTracking
title: TSPI_lineGetCallHubTracking function (tspi.h)
author: windows-sdk-content
description: The TSPI_lineGetCallHubTracking function returns the current state of CallHub tracking for the service provider. This function requires TAPI 3.0 version negotiation.
old-location: tspi\tspi_linegetcallhubtracking.htm
tech.root: Tapi
ms.assetid: c8fd8070-7393-4a59-9416-63acdd94f4ff
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TSPI_lineGetCallHubTracking, TSPI_lineGetCallHubTracking function [TAPI 2.2], _tspi_tspi_linegetcallhubtracking, tspi.tspi_linegetcallhubtracking, tspi/TSPI_lineGetCallHubTracking
ms.topic: function
f1_keywords: 
 - "tspi/TSPI_lineGetCallHubTracking"
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
 - TSPI_lineGetCallHubTracking
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TSPI_lineGetCallHubTracking function


## -description


The 
<b>TSPI_lineGetCallHubTracking</b> function returns the current state of CallHub tracking for the service provider. This function requires TAPI 3.0 version negotiation.


## -parameters




### -param hdLine

The service provider's handle to the call whose call information is to be retrieved. The call state of <i>hdLine</i> can be any state.


### -param lpTrackingInfo

A pointer to the variably sized 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linecallhubtrackinginfo">LINECALLHUBTRACKINGINFO</a> structure. Upon successful completion of the request, this structure is filled with call-related information.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/callhub-support">CallHub Tracking</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi/ns-tapi-linecallhubtrackinginfo">LINECALLHUBTRACKINGINFO</a>
 

 

