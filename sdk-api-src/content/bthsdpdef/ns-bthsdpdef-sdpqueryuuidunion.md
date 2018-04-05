---
UID: NS:bthsdpdef.SdpQueryUuidUnion
title: SdpQueryUuidUnion
author: windows-driver-content
description: The SdpQueryUuidUnion union contains the UUID on which to perform an SDP query. Used in conjunction with the SdpQueryUuid structure.
old-location: bluetooth\sdpqueryuuidunion.htm
old-project: Bluetooth
ms.assetid: 446b0337-ea83-4d8a-bee7-3cccf03e61a5
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: SdpQueryUuidUnion, SdpQueryUuidUnion structure [Bluetooth], bluetooth.sdpqueryuuidunion, bthsdpdef/SdpQueryUuidUnion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bthsdpdef.h
req.include-header: 
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
req.typenames: SdpQueryUuidUnion
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Bthsdpdef.h
api_name:
-	SdpQueryUuidUnion
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


### -field uuid32

UUID in 32-bit format.


### -field uuid16

UUID in 16-bit format.


### -field switch_type

 




## -see-also




<a href="https://msdn.microsoft.com/b208b7d6-305c-4acc-9c89-75721ff5dcb2">BTH_QUERY_SERVICE</a>



<a href="https://msdn.microsoft.com/8c67b1b1-d289-4273-a512-589b19cd1f85">SdpQueryUuid</a>
 

 

