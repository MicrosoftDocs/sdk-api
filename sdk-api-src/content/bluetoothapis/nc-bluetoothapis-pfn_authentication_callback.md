---
UID: NC:bluetoothapis.PFN_AUTHENTICATION_CALLBACK
title: PFN_AUTHENTICATION_CALLBACK
author: windows-sdk-content
description: Used in conjunction with the BluetoothRegisterForAuthentication function.
old-location: bluetooth\pfn_authentication_callback.htm
old-project: bluetooth
ms.assetid: 756bfea7-ad03-4fba-b591-42796e7d52ff
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PFN_AUTHENTICATION_CALLBACK, PFN_AUTHENTICATION_CALLBACK callback, PFN_AUTHENTICATION_CALLBACK callback function [Bluetooth], bluetooth.pfn_authentication_callback, bluetoothapis/PFN_AUTHENTICATION_CALLBACK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
req.typenames: BITS_FILE_PROPERTY_VALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - BluetoothAPIs.h
api_name:
 - PFN_AUTHENTICATION_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PFN_AUTHENTICATION_CALLBACK callback function


## -description


The <b>PFN_AUTHENTICATION_CALLBACK</b> function is a callback function prototype used in conjunction with the <a href="https://msdn.microsoft.com/f85dd076-9062-413f-863f-9d3baba322ad">BluetoothRegisterForAuthentication</a> function.
<div class="alert"><b>Note</b>  When developing for Windows Vista SP2 and Windows 7 the use of <a href="https://msdn.microsoft.com/835a624f-c08d-402c-940b-4443e1b38d58">PFN_AUTHENTICATION_CALLBACK_EX</a> is recommended.</div><div> </div>

## -parameters




### -param pvParam

Optional. A context pointer previously passed into the <a href="https://msdn.microsoft.com/f85dd076-9062-413f-863f-9d3baba322ad">BluetoothRegisterForAuthentication</a> function.


### -param pDevice

A remote Bluetooth device requesting authentication. The remote address is the same address used to register the callback during the previous call to the <a href="https://msdn.microsoft.com/f85dd076-9062-413f-863f-9d3baba322ad">BluetoothRegisterForAuthentication</a> function.


## -returns



The return value from this function is ignored by the system.




## -remarks



A caller can register for multiple addresses with the same callback function.




## -see-also




<a href="https://msdn.microsoft.com/f85dd076-9062-413f-863f-9d3baba322ad">BluetoothRegisterForAuthentication</a>
 

 

