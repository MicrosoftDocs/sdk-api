---
UID: NE:netfw._NETISO_ERROR_TYPE
title: NETISO_ERROR_TYPE (netfw.h)
author: windows-sdk-content
description: Specifies the type of error related to a network isolation operation.
old-location: ics\netiso_error_type.htm
tech.root: ics
ms.assetid: 0daa9d07-8a65-4254-b197-a37e6e04ce32
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NETISO_ERROR_TYPE, NETISO_ERROR_TYPE enumeration [ICS/ICF], NETISO_ERROR_TYPE_INTERNET_CLIENT, NETISO_ERROR_TYPE_INTERNET_CLIENT_SERVER, NETISO_ERROR_TYPE_MAX, NETISO_ERROR_TYPE_NONE, NETISO_ERROR_TYPE_PRIVATE_NETWORK, ics.netiso_error_type, networkisolation/NETISO_ERROR_TYPE, networkisolation/NETISO_ERROR_TYPE_INTERNET_CLIENT, networkisolation/NETISO_ERROR_TYPE_INTERNET_CLIENT_SERVER, networkisolation/NETISO_ERROR_TYPE_MAX, networkisolation/NETISO_ERROR_TYPE_NONE, networkisolation/NETISO_ERROR_TYPE_PRIVATE_NETWORK
ms.topic: enum
req.header: netfw.h
req.include-header: Netfw.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - HeaderDef
api_location:
 - networkisolation.h
api_name:
 - NETISO_ERROR_TYPE
product: Windows
targetos: Windows
req.typenames: NETISO_ERROR_TYPE
req.redist: 
---

# NETISO_ERROR_TYPE enumeration


## -description


The <b>NETISO_ERROR_TYPE</b> enumerated type specifies the type of error related to a network isolation operation.


## -enum-fields




### -field NETISO_ERROR_TYPE_NONE

No error.


### -field NETISO_ERROR_TYPE_PRIVATE_NETWORK

The failure was caused because the privateNetworkClientServer capability is missing.


### -field NETISO_ERROR_TYPE_INTERNET_CLIENT

The failure was caused because the internetClient capability is missing.


### -field NETISO_ERROR_TYPE_INTERNET_CLIENT_SERVER

The failure was caused because the internetClientServer capability is missing.


### -field NETISO_ERROR_TYPE_MAX

Maximum value for testing purposes.


## -see-also




<a href="https://msdn.microsoft.com/fb59b2bb-03c1-472d-bb97-6fd9d5f7169d">NetworkIsolationDiagnoseConnectFailureAndGetInfo</a>
 

 

