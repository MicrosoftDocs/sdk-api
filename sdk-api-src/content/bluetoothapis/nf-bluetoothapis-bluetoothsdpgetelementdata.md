---
UID: NF:bluetoothapis.BluetoothSdpGetElementData
title: BluetoothSdpGetElementData function (bluetoothapis.h)
description: Retrieves and parses a single element from an SDP stream.
helpviewer_keywords: ["BluetoothSdpGetElementData","BluetoothSdpGetElementData function [Bluetooth]","bluetooth.bluetoothsdpgetelementdata","bluetoothapis/BluetoothSdpGetElementData"]
old-location: bluetooth\bluetoothsdpgetelementdata.htm
tech.root: bluetooth
ms.assetid: 65de8f2f-1781-44fa-87a9-21aa461eb8ee
ms.date: 12/05/2018
ms.keywords: BluetoothSdpGetElementData, BluetoothSdpGetElementData function [Bluetooth], bluetooth.bluetoothsdpgetelementdata, bluetoothapis/BluetoothSdpGetElementData
req.header: bluetoothapis.h
req.include-header: Bthsdpdef.h, BluetoothAPIs.h
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
req.lib: Bthprops.lib
req.dll: bthprops.cpl
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BluetoothSdpGetElementData
 - bluetoothapis/BluetoothSdpGetElementData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - bthprops.cpl
 - BluetoothAPIs.dll
 - Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
 - BluetoothSdpGetElementData
---

# BluetoothSdpGetElementData function


## -description

The <b>BluetoothSdpGetElementData</b> function retrieves and parses a single element from an SDP stream.

## -parameters

### -param pSdpStream [in]

A pointer to a valid SDP stream.

### -param cbSdpStreamLength [in]

The length, in bytes, of <i>pSdpStream</i>.

### -param pData [out]

A pointer to a buffer to be filled with the data of the SDP element found at the beginning of the <i>pSdpStream</i> SDP stream.

## -returns

Returns <b>ERROR_SUCCESS</b> when the SDP element is parsed correctly. Returns <b>ERROR_INVALID_PARAMETER</b> if one of the required parameters is <b>NULL</b>, or if the SDP stream pointed to by <i>pSdpStream</i> is not valid.

## -see-also

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpenumattributes">BluetoothSdpEnumAttributes</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetcontainerelementdata">BluetoothSdpGetContainerElementData</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetstring">BluetoothSdpGetString</a>



<a href="/windows/desktop/api/bluetoothapis/ns-bluetoothapis-sdp_element_data">SDP_ELEMENT_DATA</a>



<a href="/windows/desktop/api/bluetoothapis/ns-bluetoothapis-sdp_string_type_data">SDP_STRING_TYPE_DATA</a>