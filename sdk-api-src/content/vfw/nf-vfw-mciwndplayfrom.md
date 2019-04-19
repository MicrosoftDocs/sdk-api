---
UID: NF:vfw.MCIWndPlayFrom
title: MCIWndPlayFrom macro (vfw.h)
author: windows-sdk-content
description: The MCIWndPlayFrom macro plays the content of an MCI device from the specified location to the end of the content or until another command stops playback. You can use this macro or explicitly send the MCIWNDM_PLAYFROM message.
old-location: multimedia\mciwndplayfrom.htm
tech.root: Multimedia
ms.assetid: b3efd0c9-d216-4b16-818d-76f3bb8f627e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MCIWndPlayFrom, MCIWndPlayFrom macro [Windows Multimedia], _win32_MCIWndPlayFrom, multimedia.mciwndplayfrom, vfw/MCIWndPlayFrom
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
 - MCIWndPlayFrom
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MCIWndPlayFrom macro


## -description



The <b>MCIWndPlayFrom</b> macro plays the content of an MCI device from the specified location to the end of the content or until another command stops playback. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/1c47f8eb-2a1b-4671-a9f8-fd6d59a5c7c6">MCIWNDM_PLAYFROM</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lPos

Starting location. The units for the starting location depend on the current time format. 


## -remarks



You can also specify both a starting and ending location for playback by using the <a href="https://msdn.microsoft.com/a592c28c-322f-4fd1-90e9-632703bf40c1">MCIWndPlayFromTo</a> macro.



