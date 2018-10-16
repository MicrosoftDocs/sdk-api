---
UID: NE:ipsectypes.IPSEC_FAILURE_POINT_
title: IPSEC_FAILURE_POINT_
author: windows-sdk-content
description: At what point IPsec has failed.
old-location: fwp\ipsec_failure_point.htm
tech.root: fwp
ms.assetid: 750a5643-1157-4d15-9564-127756cd08cd
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IPSEC_FAILURE_ME, IPSEC_FAILURE_NONE, IPSEC_FAILURE_PEER, IPSEC_FAILURE_POINT, IPSEC_FAILURE_POINT enumeration [Filtering], IPSEC_FAILURE_POINT_, IPSEC_FAILURE_POINT_MAX, fwp.ipsec_failure_point, ipsectypes/IPSEC_FAILURE_ME, ipsectypes/IPSEC_FAILURE_NONE, ipsectypes/IPSEC_FAILURE_PEER, ipsectypes/IPSEC_FAILURE_POINT, ipsectypes/IPSEC_FAILURE_POINT_MAX
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Ipsectypes.h
api_name:
 - IPSEC_FAILURE_POINT
product: Windows
targetos: Windows
req.typenames: IPSEC_FAILURE_POINT
req.redist: 
---

# IPSEC_FAILURE_POINT_ enumeration


## -description


The <b>IPSEC_FAILURE_POINT</b> enumerated type specifies at what point IPsec has failed.


## -enum-fields




### -field IPSEC_FAILURE_NONE

IPsec has not failed.


### -field IPSEC_FAILURE_ME

The local system is the failure point.


### -field IPSEC_FAILURE_PEER

A peer system is the failure point.


### -field IPSEC_FAILURE_POINT_MAX

Maximum value for testing only. 



## -see-also




<a href="https://msdn.microsoft.com/39029412-18ce-426a-a79d-cf25ff0dfe0d">Windows Filtering Platform API Enumerated Types</a>
 

 

