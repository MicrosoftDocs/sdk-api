---
UID: NS:iads.__MIDL___MIDL_itf_ads_0000_0000_0007
title: "__MIDL___MIDL_itf_ads_0000_0000_0007"
author: windows-driver-content
description: The ADS_TIMESTAMP structure is an ADSI representation of the Timestamp attribute syntax.
old-location: adsi\ads_timestamp.htm
old-project: ADSI
ms.assetid: 3e416a9a-e444-43eb-9e59-e8e91ccac2d9
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PADS_TIMESTAMP, ADS_TIMESTAMP, ADS_TIMESTAMP structure [ADSI], PADS_TIMESTAMP, PADS_TIMESTAMP structure pointer [ADSI], __MIDL___MIDL_itf_ads_0000_0000_0007, _ds_ads_timestamp, adsi.ads__timestamp, adsi.ads_timestamp, iads/ADS_TIMESTAMP, iads/PADS_TIMESTAMP"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ADS_TIMESTAMP, *PADS_TIMESTAMP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iads.h
api_name:
-	ADS_TIMESTAMP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# __MIDL___MIDL_itf_ads_0000_0000_0007 structure


## -description


The <b>ADS_TIMESTAMP</b> structure is an ADSI representation of the <b>Timestamp</b> attribute syntax.


## -struct-fields




### -field WholeSeconds

Number of seconds, with zero value being equal to 12:00 AM, January, 1970, UTC.


### -field EventID

An event identifier, in the order of occurrence, within the period specified by <b>WholeSeconds</b>.


## -see-also




<a href="https://msdn.microsoft.com/3ee0e469-9932-4135-8798-27d318011786">ADSI Structures</a>
 

 

