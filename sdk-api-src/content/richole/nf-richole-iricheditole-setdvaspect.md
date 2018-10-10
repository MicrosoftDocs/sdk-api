---
UID: NF:richole.IRichEditOle.SetDvaspect
title: IRichEditOle::SetDvaspect
author: windows-sdk-content
description: Sets the aspect that a rich edit control uses to draw an object. This call does not change the drawing information cached in the object; this must be done by the caller. The call does cause the object to be redrawn.
old-location: controls\IRichEditOle_SetDvaspect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditolesetdvaspect.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IRichEditOle interface [Windows Controls],SetDvaspect method, IRichEditOle.SetDvaspect, IRichEditOle::SetDvaspect, SetDvaspect, SetDvaspect method [Windows Controls], SetDvaspect method [Windows Controls],IRichEditOle interface, _win32_IRichEditOle_SetDvaspect, _win32_IRichEditOle_SetDvaspect_cpp, controls.IRichEditOle_SetDvaspect, controls._win32_IRichEditOle_SetDvaspect, richole/IRichEditOle::SetDvaspect
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
 - IRichEditOle.SetDvaspect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRichEditOle::SetDvaspect


## -description


Sets the aspect that a rich edit control uses to draw an object. This call does not change the drawing information cached in the object; this must be done by the caller. The call does cause the object to be redrawn.


## -parameters




### -param iob

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Index of the object whose aspect is to be set. If this parameter is REO_IOB_SELECTION, the aspect of the selected object is to be set. 


### -param dvaspect

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Aspect to use when drawing. The values are defined by OLE. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK on success, or a failure code otherwise. E_INVALIDARG is returned if the index is invalid.




## -see-also




<a href="https://msdn.microsoft.com/d6d1794b-f16c-4a8c-84f5-dfe8bd8be08c">IRichEditOle</a>
 

 

