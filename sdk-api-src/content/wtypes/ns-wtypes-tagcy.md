---
UID: NS:wtypes.tagCY
title: tagCY
author: windows-sdk-content
description: A currency number stored as an 8-byte, two's complement integer, scaled by 10,000 to give a fixed-point number with 15 digits to the left of the decimal point and 4 digits to the right.
old-location: automat\currency.htm
tech.root: automat
ms.assetid: 5e81273c-7289-45c7-93c0-32c1553f708e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPCY, CURRENCY, CURRENCY union [Automation], CY, CY union [Automation], _oa96_CURRENCY, automat.currency, tagCY, wtypes/CURRENCY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wtypes.h
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
 - HeaderDef
api_location:
 - Wtypes.h
api_name:
 - CY
product: Windows
targetos: Windows
req.typenames: CY
req.redist: 
---

# tagCY structure


## -description


A currency number stored as an 8-byte, two's complement integer, scaled by 10,000 to give a fixed-point number with 15 digits to the left of the decimal point and 4 digits to the right. This <b>IDispatch::GetTypeInfo</b> resentation provides a range of 922337203685477.5807 to -922337203685477.5808.

The CURRENCY data type is useful for calculations involving money, or for any fixed-point calculation where accuracy is particularly important.


## -struct-fields




### -field int64


#### - Hi


#### - Lo

