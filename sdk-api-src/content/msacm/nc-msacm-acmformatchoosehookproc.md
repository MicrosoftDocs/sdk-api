---
UID: NC:msacm.ACMFORMATCHOOSEHOOKPROC
title: ACMFORMATCHOOSEHOOKPROC
author: windows-driver-content
description: The acmFormatChooseHookProc function specifies a user-defined function that hooks the acmFormatChoose dialog box. The acmFormatChooseHookProc name is a placeholder for an application-defined name.
old-location: multimedia\acmformatchoosehookproc.htm
old-project: Multimedia
ms.assetid: 75b11c0f-ae85-424d-b936-492d67440659
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "_win32_acmFormatChooseHookProc, acmFormatChooseHookProc, acmFormatChooseHookProc callback, acmFormatChooseHookProc callback function [Windows Multimedia], msacm/acmFormatChooseHookProc, multimedia.acmformatchoosehookproc"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: msacm.h
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
req.typenames: SSTP_CONFIG_PARAMS, *PSSTP_CONFIG_PARAMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Msacm.h
api_name:
-	acmFormatChooseHookProc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ACMFORMATCHOOSEHOOKPROC callback function


## -description



The <b>acmFormatChooseHookProc</b> function specifies a user-defined function that hooks the <a href="https://msdn.microsoft.com/9be8311a-f6ad-4007-a254-841ee99ff3b6">acmFormatChoose</a> dialog box. The <b>acmFormatChooseHookProc</b> name is a placeholder for an application-defined name.




## -parameters




### -param hwnd

Window handle for the dialog box.


### -param uMsg

Window message.


### -param wParam

Message parameter.


### -param lParam

Message parameter.


## -remarks



If the hook function processes one of the WM_CTLCOLOR messages, this function must return a handle of the brush that should be used to paint the control background.

A hook function can optionally process the MM_ACM_FORMATCHOOSE message.

You should use this function the same way as you use the Common Dialog hook functions for customizing common dialog boxes.




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

