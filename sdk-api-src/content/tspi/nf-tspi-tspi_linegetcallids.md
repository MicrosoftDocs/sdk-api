---
UID: NF:tspi.TSPI_lineGetCallIDs
title: TSPI_lineGetCallIDs function (tspi.h)
author: windows-sdk-content
description: The TSPI_lineGetCallIDs function returns the call identifiers for the service provider. This function requires TAPI 3.0 version negotiation.
old-location: tspi\tspi_linegetcallids.htm
tech.root: Tapi
ms.assetid: d2a23712-a144-416c-a914-935f1776c256
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TSPI_lineGetCallIDs, TSPI_lineGetCallIDs function [TAPI 2.2], _tspi_tspi_linegetcallids, tspi.tspi_linegetcallids, tspi/TSPI_lineGetCallIDs
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
 - TSPI_lineGetCallIDs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/29b6e585-6da8-46a2-a612-f42d0f65f68e">CallHub Tracking</a>



<a href="https://msdn.microsoft.com/1f4eaf7d-fc80-4131-af5a-30c6869c74ef">LINECALLHUBTRACKINGINFO</a>
 

 

