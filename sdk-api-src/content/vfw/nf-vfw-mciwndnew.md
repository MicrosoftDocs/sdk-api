---
UID: NF:vfw.MCIWndNew
title: MCIWndNew macro (vfw.h)
author: windows-sdk-content
description: The MCIWndNew macro creates a new file for the current MCI device. You can use this macro or explicitly send the MCIWNDM_NEW message.
old-location: multimedia\mciwndnew.htm
tech.root: Multimedia
ms.assetid: dddd73d5-3ce5-43df-a685-05f519b45386
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MCIWndNew, MCIWndNew macro [Windows Multimedia], _win32_MCIWndNew, multimedia.mciwndnew, vfw/MCIWndNew
ms.topic: macro
f1_keywords: 
 - "vfw/MCIWndNew"
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
 - MCIWndNew
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MCIWndNew macro


## -description



The <b>MCIWndNew</b> macro creates a new file for the current MCI device. You can use this macro or explicitly send the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mciwndm-new">MCIWNDM_NEW</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lp

Pointer to a buffer containing the name of the MCI device that will use the file. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mciwndm-new">MCIWNDM_NEW</a>
 

 

