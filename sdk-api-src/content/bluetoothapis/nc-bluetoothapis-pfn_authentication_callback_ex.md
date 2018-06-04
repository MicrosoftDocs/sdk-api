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
 

 

