---
UID: NF:tspi.TSPI_lineGetAddressStatus
title: TSPI_lineGetAddressStatus function
author: windows-sdk-content
description: The TSPI_lineGetAddressStatus function queries the specified address for its current status.
old-location: tspi\tspi_linegetaddressstatus.htm
old-project: tapi
ms.assetid: e3afd959-a0cb-4f0a-a700-d50cf7a4c386
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: TSPI_lineGetAddressStatus, TSPI_lineGetAddressStatus function [TAPI 2.2], _tspi_tspi_linegetaddressstatus, tspi.tspi_linegetaddressstatus, tspi/TSPI_lineGetAddressStatus
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AAAccountingData
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineGetAddressStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TSPI_lineGetAddressStatus function


## -description


The 
<b>TSPI_lineGetAddressStatus</b> function queries the specified address for its current status.


## -parameters




### -param hdLine

The service provider's handle to the line containing the address to be queried.


### -param dwAddressID

An address on the given open line device. This is the address to be queried. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades. This parameter is not validated by TAPI when this function is called.


### -param lpAddressStatus

A pointer to a variably sized data structure of type 
<a href="https://msdn.microsoft.com/795aa97d-76a9-4041-b9f6-345644561043">LINEADDRESSSTATUS</a>.


## -returns



Returns zero if the function succeeds or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALLINEHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALADDRESSID, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.




## -remarks



The service provider fills in all the members of the 
<a href="https://msdn.microsoft.com/795aa97d-76a9-4041-b9f6-345644561043">LINEADDRESSSTATUS</a> data structure, except for <b>dwTotalSize</b>, which is filled in by TAPI. The service provider must not overwrite the <b>dwTotalSize</b> member.




## -see-also




<a href="https://msdn.microsoft.com/795aa97d-76a9-4041-b9f6-345644561043">LINEADDRESSSTATUS</a>
 

 

