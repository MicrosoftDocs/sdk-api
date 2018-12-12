---
UID: NF:richole.IRichEditOle.ContextSensitiveHelp
title: IRichEditOle::ContextSensitiveHelp
author: windows-sdk-content
description: Indicates if a rich edit control should transition into or out of context-sensitive help mode. A rich edit control calls the IRichEditOle::ContextSensitiveHelp method of any in-place object which is currently active if a state change is occurring.
old-location: controls\IRichEditOle_ContextSensitiveHelp.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditolecontextsensitivehelp.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ContextSensitiveHelp, ContextSensitiveHelp method [Windows Controls], ContextSensitiveHelp method [Windows Controls],IRichEditOle interface, IRichEditOle interface [Windows Controls],ContextSensitiveHelp method, IRichEditOle.ContextSensitiveHelp, IRichEditOle::ContextSensitiveHelp, _win32_IRichEditOle_ContextSensitiveHelp, _win32_IRichEditOle_ContextSensitiveHelp_cpp, controls.IRichEditOle_ContextSensitiveHelp, controls._win32_IRichEditOle_ContextSensitiveHelp, richole/IRichEditOle::ContextSensitiveHelp
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: richole.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - IRichEditOle.ContextSensitiveHelp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRichEditOle::ContextSensitiveHelp


## -description


Indicates if a rich edit control should transition into or out of context-sensitive help mode. A rich edit control calls the <b>IRichEditOle::ContextSensitiveHelp</b> method of any in-place object which is currently active if a state change is occurring.


## -parameters




### -param fEnterMode

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Indicator of whether the control is entering context-sensitive help mode (<b>TRUE</b>) or leaving it (<b>FALSE</b>). 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK on success, or a failure code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb774306(v=VS.85).aspx">IRichEditOle</a>
 

 

