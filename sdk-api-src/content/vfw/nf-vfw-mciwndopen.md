---
UID: NF:vfw.MCIWndOpen
title: MCIWndOpen macro
author: windows-sdk-content
description: The MCIWndOpen macro opens an MCI device and associates it with an MCIWnd window.
old-location: multimedia\mciwndopen.htm
tech.root: Multimedia
ms.assetid: 88620085-8cba-489c-bfb8-d28b0a5e6013
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: MCIWndOpen, MCIWndOpen macro [Windows Multimedia], _win32_MCIWndOpen, multimedia.mciwndopen, vfw/MCIWndOpen
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - MCIWndOpen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MCIWndOpen macro


## -description



The <b>MCIWndOpen</b> macro opens an MCI device and associates it with an MCIWnd window. For MCI devices that use data files, this macro can also open a specified data file, name a new file to be created, or display a dialog box to let the user select a file to open. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057">MCIWNDM_OPEN</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param sz

Pointer to a null-terminated string identifying the filename or MCI Device Names to open. Specify â€“1 for this parameter to display the Open dialog box. 


### -param f

Flags associated with the device or file to open. The MCIWNDOPENF_NEW flag specifies a new file is to be created with the name specified in szFile. 

