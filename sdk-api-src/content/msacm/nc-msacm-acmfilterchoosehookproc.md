---
UID: NC:msacm.ACMFILTERCHOOSEHOOKPROC
title: ACMFILTERCHOOSEHOOKPROC
author: windows-sdk-content
description: The acmFilterChooseHookProc function specifies a user-defined function that hooks the acmFilterChoose dialog box.
old-location: multimedia\acmfilterchoosehookproc.htm
tech.root: Multimedia
ms.assetid: 974bdf53-cd1e-433b-9d49-8dfc20254ebf
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "_win32_acmFilterChooseHookProc, acmFilterChooseHookProc, acmFilterChooseHookProc callback, acmFilterChooseHookProc callback function [Windows Multimedia], msacm/acmFilterChooseHookProc, multimedia.acmfilterchoosehookproc"
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Msacm.h
api_name:
 - acmFilterChooseHookProc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ACMFILTERCHOOSEHOOKPROC callback function


## -description



The <b>acmFilterChooseHookProc</b> function specifies a user-defined function that hooks the <a href="https://msdn.microsoft.com/9d8f659f-46f7-4399-a538-24c887c0fbee">acmFilterChoose</a> dialog box.




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



To customize the dialog box selections, a hook function can optionally process the MM_ACM_FILTERCHOOSE message.

You should use this function the same way as you use the Common Dialog hook functions for customizing common dialog boxes.




## -see-also




<a href="https://msdn.microsoft.com/da207a50-9c67-4cf3-920b-5878637060db">Audio Compression Functions</a>



<a href="https://msdn.microsoft.com/2f9a4540-86c0-40e6-b4da-24a9d31b56bf">Audio Compression Manager</a>
 

 

