---
UID: NF:bluetoothapis.BluetoothSdpGetContainerElementData
title: BluetoothSdpGetContainerElementData function
author: windows-sdk-content
description: Iterates a container stream and returns each element contained within the container element.
old-location: bluetooth\bluetoothsdpgetcontainerelementdata.htm
old-project: Bluetooth
ms.assetid: 7dbf44f6-8a80-419e-9db7-60ada9ca9647
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: BluetoothSdpGetContainerElementData, BluetoothSdpGetContainerElementData function [Bluetooth], bluetooth.bluetoothsdpgetcontainerelementdata, bluetoothapis/BluetoothSdpGetContainerElementData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: BLUETOOTH_IO_CAPABILITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Bthprops.dll
-	BluetoothAPIs.dll
-	Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
-	BluetoothSdpGetContainerElementData
product: Windows
targetos: Windows
req.lib: Bthprops.lib
req.dll: Bthprops.dll
req.irql: 
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
          time the <b>BluetoothSdpGetContainerElementData</b> function is called for a  container, *<i>pElement</i>
should be <b>NULL</b>.  For subsequent calls, the value should be
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
the <a href="https://msdn.microsoft.com/7dbf44f6-8a80-419e-9db7-60ada9ca9647">BluetoothSdpGetContainerElementData</a> function for this container.

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




<a href="https://msdn.microsoft.com/3113db03-a32f-47ad-a442-3769f41ee8e7">BluetoothSdpEnumAttributes</a>



<a href="https://msdn.microsoft.com/65de8f2f-1781-44fa-87a9-21aa461eb8ee">BluetoothSdpGetElementData</a>



<a href="https://msdn.microsoft.com/26a68fe3-6ffb-44ff-b9db-757d35022a41">BluetoothSdpGetString</a>



<a href="https://msdn.microsoft.com/9c9d6103-cc49-41d2-bbb3-6b6888fb93e7">SDP_ELEMENT_DATA</a>



<a href="https://msdn.microsoft.com/16ff7951-08a7-49c5-93a5-0782cca50dab">SDP_STRING_TYPE_DATA</a>
 

 

