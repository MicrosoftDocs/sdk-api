---
UID: NC:bluetoothapis.PFN_AUTHENTICATION_CALLBACK_EX
title: PFN_AUTHENTICATION_CALLBACK_EX
author: windows-sdk-content
description: PFN_AUTHENTICATION_CALLBACK_EX function is a callback function prototype used in conjunction with the BluetoothRegisterForAuthenticationEx function.
old-location: bluetooth\pfn_authentication_callback_ex.htm
tech.root: Bluetooth
ms.assetid: 835a624f-c08d-402c-940b-4443e1b38d58
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PFN_AUTHENTICATION_CALLBACK_EX, PFN_AUTHENTICATION_CALLBACK_EX callback, PFN_AUTHENTICATION_CALLBACK_EX callback function [Bluetooth], bluetooth.pfn_authentication_callback_ex, bluetoothapis/PFN_AUTHENTICATION_CALLBACK_EX
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - BluetoothAPIs.h
api_name:
 - PFN_AUTHENTICATION_CALLBACK_EX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_AUTHENTICATION_CALLBACK_EX callback function


## -description


The <i>PFN_AUTHENTICATION_CALLBACK_EX</i> function is a callback function prototype  used in conjunction with the <a href="https://msdn.microsoft.com/c9838f27-3450-4d51-be58-ce515d06d5cb">BluetoothRegisterForAuthenticationEx</a> function.
<div class="alert"><b>Note</b>  This structure is supported in Windows Vista SP2 and Windows 7.</div><div> </div>

## -parameters




### -param pvParam [in, optional]

Optional. A context pointer previously passed into the <a href="https://msdn.microsoft.com/f85dd076-9062-413f-863f-9d3baba322ad">BluetoothRegisterForAuthentication</a> function.


### -param pAuthCallbackParams [in]

A <a href="https://msdn.microsoft.com/e9c703c1-7981-4c34-a96e-0123d3655e55">BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS</a> structure that contains device and authentication configuration information specific to the Bluetooth device responding to an authentication request.


## -returns



The return value from this function is ignored by the system.




## -see-also




<a href="https://msdn.microsoft.com/c9838f27-3450-4d51-be58-ce515d06d5cb">BluetoothRegisterForAuthenticationEx</a>



<a href="https://msdn.microsoft.com/756bfea7-ad03-4fba-b591-42796e7d52ff">PFN_AUTHENTICATION_CALLBACK</a>
 

 

