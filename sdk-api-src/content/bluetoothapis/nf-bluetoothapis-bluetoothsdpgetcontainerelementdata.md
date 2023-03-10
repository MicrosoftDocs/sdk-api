---
UID: NF:bluetoothapis.BluetoothSdpGetContainerElementData
title: BluetoothSdpGetContainerElementData function (bluetoothapis.h)
description: Iterates a container stream and returns each element contained within the container element.
helpviewer_keywords: ["BluetoothSdpGetContainerElementData","BluetoothSdpGetContainerElementData function [Bluetooth]","bluetooth.bluetoothsdpgetcontainerelementdata","bluetoothapis/BluetoothSdpGetContainerElementData"]
old-location: bluetooth\bluetoothsdpgetcontainerelementdata.htm
tech.root: bluetooth
ms.assetid: 7dbf44f6-8a80-419e-9db7-60ada9ca9647
ms.date: 12/05/2018
ms.keywords: BluetoothSdpGetContainerElementData, BluetoothSdpGetContainerElementData function [Bluetooth], bluetooth.bluetoothsdpgetcontainerelementdata, bluetoothapis/BluetoothSdpGetContainerElementData
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
 - BluetoothSdpGetContainerElementData
 - bluetoothapis/BluetoothSdpGetContainerElementData
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
 - BluetoothSdpGetContainerElementData
---

# BluetoothSdpGetContainerElementData function


## -description

The <b>BluetoothSdpGetContainerElementData</b> function iterates a container stream and returns each element contained within the container element.

## -parameters

### -param pContainerStream [in]

A pointer to valid SDP stream. The first element in the stream must be a sequence
or an alternative.

### -param cbContainerLength [in]

The size, in bytes, of the <i>pContainerStream</i> parameter.

### -param pElement [in, out]

A value used to track the  location in the stream.  The first
          time the <b>BluetoothSdpGetContainerElementData</b> function is called for a  container, *<i>pElement</i> should be <b>NULL</b>.  For subsequent calls, the value should be
unmodified.

### -param pData [out]

A pointer to a buffer filled with data from  the
current SDP element of <i>pContainerStream</i>.

## -returns

Returns <b>ERROR_SUCCESS</b> upon success, indicating that the <i>pData</i> parameter contains the data. Returns error codes upon failure. The following table describes common error codes associated with the <b>BluetoothSdpGetContainerElementData</b> function:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more items in the list. The caller should stop calling
the <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetcontainerelementdata">BluetoothSdpGetContainerElementData</a> function for this container.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A required pointer is <b>NULL</b>, or the container is not a valid SDP
stream.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpenumattributes">BluetoothSdpEnumAttributes</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetelementdata">BluetoothSdpGetElementData</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetstring">BluetoothSdpGetString</a>



<a href="/windows/desktop/api/bluetoothapis/ns-bluetoothapis-sdp_element_data">SDP_ELEMENT_DATA</a>



<a href="/windows/desktop/api/bluetoothapis/ns-bluetoothapis-sdp_string_type_data">SDP_STRING_TYPE_DATA</a>