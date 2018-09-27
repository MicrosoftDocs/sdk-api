---
UID: NF:tspi.TSPI_lineSetCallHubTracking
title: TSPI_lineSetCallHubTracking function
author: windows-sdk-content
description: The TSPI_lineSetCallHubTracking function sets the CallHub tracking mode. This function requires TAPI 3.0 version negotiation.
old-location: tspi\tspi_linesetcallhubtracking.htm
tech.root: tapi
ms.assetid: ec2d5d46-1c83-47a0-9c10-684959630a16
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: TSPI_lineSetCallHubTracking, TSPI_lineSetCallHubTracking function [TAPI 2.2], _tspi_tspi_linesetcallhubtracking, tspi.tspi_linesetcallhubtracking, tspi/TSPI_lineSetCallHubTracking
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/1f4eaf7d-fc80-4131-af5a-30c6869c74ef">LINECALLHUBTRACKINGINFO</a>. Upon successful completion of the request, this structure is filled with call-related information.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL




## -see-also




<a href="https://msdn.microsoft.com/ea23ae25-2fbb-4060-8273-cd7921d49e52">CallHub Object</a>



<a href="https://msdn.microsoft.com/1f4eaf7d-fc80-4131-af5a-30c6869c74ef">LINECALLHUBTRACKINGINFO</a>
 

 

