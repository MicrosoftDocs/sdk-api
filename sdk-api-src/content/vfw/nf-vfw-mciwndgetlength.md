---
UID: NF:vfw.MCIWndGetLength
title: MCIWndGetLength macro
author: windows-sdk-content
description: The MCIWndGetLength macro retrieves the length of the content or file currently used by an MCI device. You can use this macro or explicitly send the MCIWNDM_GETLENGTH message.
old-location: multimedia\mciwndgetlength.htm
old-project: Multimedia
ms.assetid: 2d027660-b2dd-4613-9583-30d7a45f7a1d
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: MCIWndGetLength, MCIWndGetLength macro [Windows Multimedia], _win32_MCIWndGetLength, multimedia.mciwndgetlength, vfw/MCIWndGetLength
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - MCIWndGetLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# MCIWndGetLength macro


## -description



The <b>MCIWndGetLength</b> macro retrieves the length of the content or file currently used by an MCI device. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f">MCIWNDM_GETLENGTH</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


## -remarks



This value added to the value returned for the <a href="https://msdn.microsoft.com/fe9346b8-e917-4bbc-9df5-3b0b5c2de306">MCIWndGetStart</a> macro equals the end of the content.




## -see-also




<a href="https://msdn.microsoft.com/bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f">MCIWNDM_GETLENGTH</a>



<a href="https://msdn.microsoft.com/fe9346b8-e917-4bbc-9df5-3b0b5c2de306">MCIWndGetStart</a>
 

 

