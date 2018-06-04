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

# MCIWndOpen macro


## -description



The <b>MCIWndOpen</b> macro opens an MCI device and associates it with an MCIWnd window. For MCI devices that use data files, this macro can also open a specified data file, name a new file to be created, or display a dialog box to let the user select a file to open. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057">MCIWNDM_OPEN</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param sz

TBD


### -param f

TBD






#### - szFile

Pointer to a null-terminated string identifying the filename or MCI Device Names to open. Specify â€“1 for this parameter to display the Open dialog box. 


#### - wFlags

Flags associated with the device or file to open. The MCIWNDOPENF_NEW flag specifies a new file is to be created with the name specified in szFile. 

