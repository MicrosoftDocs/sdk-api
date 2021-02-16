---
UID: NS:ws2bth._BTH_QUERY_DEVICE
title: BTH_QUERY_DEVICE (ws2bth.h)
description: The BTH_QUERY_DEVICE structure is used when querying for the presence of a Bluetooth device.
helpviewer_keywords: ["*PBTHNS_INQUIRYBLOB","*PBTH_QUERY_DEVICE","BTHNS_INQUIRYBLOB","BTH_QUERY_DEVICE","BTH_QUERY_DEVICE structure [Bluetooth]","PBTH_QUERY_DEVICE","PBTH_QUERY_DEVICE structure pointer [Bluetooth]","_bth_bth_query_device","bluetooth.bth_query_device","ws2bth/BTH_QUERY_DEVICE","ws2bth/PBTH_QUERY_DEVICE"]
old-location: bluetooth\bth_query_device.htm
tech.root: bluetooth
ms.assetid: c132c79e-5938-4436-a1fb-d0d6db5dc9d3
ms.date: 12/05/2018
ms.keywords: '*PBTHNS_INQUIRYBLOB, *PBTH_QUERY_DEVICE, BTHNS_INQUIRYBLOB, BTH_QUERY_DEVICE, BTH_QUERY_DEVICE structure [Bluetooth], PBTH_QUERY_DEVICE, PBTH_QUERY_DEVICE structure pointer [Bluetooth], _bth_bth_query_device, bluetooth.bth_query_device, ws2bth/BTH_QUERY_DEVICE, ws2bth/PBTH_QUERY_DEVICE'
req.header: ws2bth.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: BTH_QUERY_DEVICE, *PBTH_QUERY_DEVICE, BTHNS_INQUIRYBLOB, *PBTHNS_INQUIRYBLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BTH_QUERY_DEVICE
 - ws2bth/_BTH_QUERY_DEVICE
 - PBTH_QUERY_DEVICE
 - ws2bth/PBTH_QUERY_DEVICE
 - BTH_QUERY_DEVICE
 - ws2bth/BTH_QUERY_DEVICE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2bth.h
api_name:
 - BTH_QUERY_DEVICE
---

# BTH_QUERY_DEVICE structure


## -description

The 
<b>BTH_QUERY_DEVICE</b> structure is used when querying for the presence of a Bluetooth device.

## -struct-fields

### -field LAP

Reserved. Must be set to zero.

### -field length

Requested length of the inquiry, in seconds.

## -remarks

See the Bluetooth specification at 
<a href="https://www.bluetooth.com/">www.bluetooth.com</a> for additional information about LAP.

## -see-also

<a href="/windows/desktop/Bluetooth/bluetooth-and-wsalookupservicebegin-for-device-inquiry">Bluetooth and WSALookupServiceBegin for Device
		  Inquiry</a>



<a href="/windows/desktop/Bluetooth/bluetooth-and-wsaqueryset-for-device-inquiry">Bluetooth and WSAQUERYSET for Device Inquiry</a>