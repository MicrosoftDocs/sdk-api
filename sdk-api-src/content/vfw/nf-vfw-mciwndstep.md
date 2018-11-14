---
UID: NF:vfw.MCIWndStep
title: MCIWndStep macro
author: windows-sdk-content
description: The MCIWndStep macro moves the current position in the content forward or backward by a specified increment. You can use this macro or explicitly send the MCI_STEP command.
old-location: multimedia\mciwndstep.htm
tech.root: Multimedia
ms.assetid: 4490901c-a58c-465c-a7b3-230456848da3
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: MCIWndStep, MCIWndStep macro [Windows Multimedia], _win32_MCIWndStep, multimedia.mciwndstep, vfw/MCIWndStep
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
 - MCIWndStep
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- vfw.h
: 
- MCIWndStep
: 
---

# MCIWndStep macro


## -description



The <b>MCIWndStep</b> macro moves the current position in the content forward or backward by a specified increment. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/8d976840-fe9d-4393-b9fc-10f847166b1b">MCI_STEP</a> command.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param n

Step value. Negative values step the device through the content in reverse. The units for the step value depend on the current time format. 

