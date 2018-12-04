---
UID: NF:tspi.TSPI_lineGetNumAddressIDs
title: TSPI_lineGetNumAddressIDs function
author: windows-sdk-content
description: The TSPI_lineGetNumAddressIDs function retrieves the number of address identifiers supported on the indicated line.
old-location: tspi\tspi_linegetnumaddressids.htm
tech.root: tapi
ms.assetid: 53fd70eb-2694-4c8c-97cd-6ee9f2606ced
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: TSPI_lineGetNumAddressIDs, TSPI_lineGetNumAddressIDs function [TAPI 2.2], _tspi_tspi_linegetnumaddressids, tspi.tspi_linegetnumaddressids, tspi/TSPI_lineGetNumAddressIDs
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
 - TSPI_lineGetNumAddressIDs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_lineGetNumAddressIDs function


## -description


The 
<b>TSPI_lineGetNumAddressIDs</b> function retrieves the number of address identifiers supported on the indicated line.


## -parameters




### -param hdLine

The handle to the line for which the number of address identifiers is to be retrieved.


### -param lpdwNumAddressIDs

A pointer to a <b>DWORD</b>. The location is filled with the number of address identifiers supported on the indicated line. The value is one or larger.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL.




## -remarks



This function is called by TAPI in response to an application calling 
<a href="https://msdn.microsoft.com/d600fd39-4e58-421c-81bf-1555f5745f5e">lineSetNumRings</a>, 
<a href="https://msdn.microsoft.com/7aee6396-6045-4e7b-9df9-3729159ea4b2">lineGetNumRings</a>, or 
<a href="https://msdn.microsoft.com/179af1a1-078f-401c-8c15-12fc8ca06e3c">lineGetNewCalls</a>. TAPI uses the retrieved value to determine if the specified address identifier is within the range supported by the service provider.




## -see-also




<a href="https://msdn.microsoft.com/179af1a1-078f-401c-8c15-12fc8ca06e3c">lineGetNewCalls</a>



<a href="https://msdn.microsoft.com/7aee6396-6045-4e7b-9df9-3729159ea4b2">lineGetNumRings</a>



<a href="https://msdn.microsoft.com/d600fd39-4e58-421c-81bf-1555f5745f5e">lineSetNumRings</a>
 

 

