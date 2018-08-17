---
UID: NS:bthsdpdef.SdpQueryUuidUnion
title: SdpQueryUuidUnion
author: windows-sdk-content
description: The SdpQueryUuidUnion union contains the UUID on which to perform an SDP query. Used in conjunction with the SdpQueryUuid structure.
old-location: bluetooth\sdpqueryuuidunion.htm
old-project: bluetooth
ms.assetid: 446b0337-ea83-4d8a-bee7-3cccf03e61a5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SdpQueryUuidUnion, SdpQueryUuidUnion structure [Bluetooth], bluetooth.sdpqueryuuidunion, bthsdpdef/SdpQueryUuidUnion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: bthsdpdef.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: SdpQueryUuidUnion
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bthsdpdef.h
api_name:
 - SdpQueryUuidUnion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# SdpQueryUuidUnion structure


## -description


The <b>SdpQueryUuidUnion</b> union contains the UUID on which to perform an SDP query. Used in conjunction with the <b>SdpQueryUuid</b> structure.


## -struct-fields




### -field uuid128

UUID in 128-bit format.


### -field uuid128.case

 


### -field uuid128.case.SDP_ST_UUID128

 


### -field uuid32

UUID in 32-bit format.


### -field uuid32.case

 


### -field uuid32.case.SDP_ST_UUID32

 


### -field uuid16

UUID in 16-bit format.


### -field uuid16.case

 


### -field uuid16.case.SDP_ST_UUID16

 


### -field switch_type

 


### -field switch_type.unsigned short

 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362938(v=VS.85).aspx">BTH_QUERY_SERVICE</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362950(v=VS.85).aspx">SdpQueryUuid</a>
 

 

