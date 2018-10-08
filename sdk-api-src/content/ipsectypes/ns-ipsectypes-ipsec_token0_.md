---
UID: NS:ipsectypes.IPSEC_TOKEN0_
title: IPSEC_TOKEN0_
author: windows-sdk-content
description: Various information about an IPsec-specific access token.
old-location: fwp\ipsec_token0.htm
tech.root: fwp
ms.assetid: 12adf88e-05c7-4e08-bbf7-6da529387af1
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IPSEC_TOKEN0, IPSEC_TOKEN0 structure [Filtering], IPSEC_TOKEN0_, fwp.ipsec_token0, ipsectypes/IPSEC_TOKEN0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
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
 - Ipsectypes.h
api_name:
 - IPSEC_TOKEN0
product: Windows
targetos: Windows
req.typenames: IPSEC_TOKEN0
req.redist: 
---

# IPSEC_TOKEN0_ structure


## -description


The <b>IPSEC_TOKEN0</b> structure contains various information about an IPsec-specific access token.


## -struct-fields




### -field type

An <a href="https://msdn.microsoft.com/68eb9301-33d9-4ab9-b3e7-0fc83b6f0f1d">IPSEC_TOKEN_TYPE</a> value that specifies the type of token.


### -field principal

An <a href="https://msdn.microsoft.com/f61944aa-2545-4fdd-8bae-6271d4535acc">IPSEC_TOKEN_PRINCIPAL</a> value that specifies the token principal.


### -field mode

An <a href="https://msdn.microsoft.com/5f90e473-39e1-4eed-9ea1-1f20929d5a07">IPSEC_TOKEN_MODE</a> value that indicates in which mode the token was obtained.


### -field token

Handle to the access token.  An <b>IPSEC_TOKEN_HANDLE</b> is of type <b>UINT64</b>.


## -remarks



<b>IPSEC_TOKEN0</b> is a specific implementation of IPSEC_TOKEN. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.



