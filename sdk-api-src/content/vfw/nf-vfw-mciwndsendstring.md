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

# MCIWndSendString macro


## -description



The <b>MCIWndSendString</b> macro sends an MCI command in string form to the device associated with the MCIWnd window. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/0e999a0e-588d-4f06-a1bc-fd3f245d8980">MCIWNDM_SENDSTRING</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param sz

String command to send to the MCI device. 


## -remarks



The message handler for <b>MCIWndSendString</b> (and <b>MCIWNDM_SENDSTRING</b>) appends a device alias to the MCI command you send to the device. Therefore, you should not use any alias in an MCI command that you issue with <b>MCIWndSendString</b>.

To get the return string, which contains the result of the command, use the <a href="https://msdn.microsoft.com/8e7d54ec-882b-4896-a493-3ed61aec6184">MCIWndReturnString</a> macro.




## -see-also




<a href="https://msdn.microsoft.com/f8edfdbd-1334-4323-aec5-73c0a56f9b4d">Multimedia Command Strings</a>
 

 

