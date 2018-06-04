---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _BLUETOOTH_RADIO_INFO structure


## -description


The <b>BLUETOOTH_RADIO_INFO</b> structure contains information about a Bluetooth radio.


## -struct-fields




### -field dwSize

Size, in bytes,  of the structure.


### -field address

Address of the local Bluetooth radio.


### -field szName

Name of the local Bluetooth radio.


### -field ulClassofDevice

Device class for the local Bluetooth radio.


### -field lmpSubversion

This member contains data specific to individual Bluetooth device manufacturers.


### -field manufacturer

Manufacturer of the Bluetooth radio, expressed as a <b>BTH_MFG_Xxx</b> value. For more information about the Bluetooth assigned numbers document and a current list of values, see the Bluetooth specification at <a href="Http://go.microsoft.com/fwlink/p/?linkid=84017">www.bluetooth.com</a>.


## -see-also




<a href="https://msdn.microsoft.com/b997203d-e7e4-43aa-b751-e419483020ac">BLUETOOTH_FIND_RADIO_PARAMS</a>



<a href="https://msdn.microsoft.com/f31bb18b-c129-417f-ab87-cf114a2e094f">BluetoothFindFirstRadio</a>



<a href="https://msdn.microsoft.com/7dd6b823-f9c6-4375-80b6-d59c4570c8fb">BluetoothFindNextRadio</a>



<a href="https://msdn.microsoft.com/859771b1-d06c-414b-81cb-bb3913fd0380">BluetoothFindRadioClose</a>



<a href="https://msdn.microsoft.com/0c596f49-70f9-4a58-842c-e01dcf69bd01">BluetoothGetRadioInfo</a>



<a href="https://msdn.microsoft.com/39e41b66-44ed-46dc-bfc2-65228b669992">WSAGetLastError</a>
 

 

