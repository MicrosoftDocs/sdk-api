---
UID: NS:wtsapi32._WTS_PRODUCT_INFOW
title: "_WTS_PRODUCT_INFOW"
author: windows-sdk-content
description: The details of the product license that is required to connect to a terminal server.
old-location: termserv\wts_product_info.htm
old-project: termserv
ms.assetid: 92E4BC54-029D-4B37-9397-CFF44B9712A3
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: PRODUCT_INFO, PRODUCT_INFO structure [Remote Desktop Services], PRODUCT_INFOW, WTS_PRODUCT_INFO, WTS_PRODUCT_INFO structure [Remote Desktop Services], WTS_PRODUCT_INFOA, WTS_PRODUCT_INFOW, _WTS_PRODUCT_INFOA, _WTS_PRODUCT_INFOW, termserv.wts_product_info, wtsapi32/WTS_PRODUCT_INFO, wtsapi32/WTS_PRODUCT_INFOA, wtsapi32/WTS_PRODUCT_INFOW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTS_PRODUCT_INFOW (Unicode) and WTS_PRODUCT_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRODUCT_INFOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsapi32.h
api_name:
 - PRODUCT_INFO
 - WTS_PRODUCT_INFOA
 - WTS_PRODUCT_INFOW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WTS_PRODUCT_INFOW structure


## -description


 The details of the product license that is required to connect to a  terminal server.


## -struct-fields




### -field CompanyName

An array that contains the company name.


### -field ProductID

 




#### - CHAR

An array that specifies the type of the license that is required by the terminal server.


This member can contain the following value:





#### "A02"

Per device or per user license


##### - CHAR."A02"

Per device or per user license


## -remarks



<b>PRODUCTINFO_COMPANYNAME_LENGTH</b> is 256.

<b>PRODUCTINFO_PRODUCTID_LENGTH</b> is 4.



