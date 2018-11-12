---
UID: NF:richole.IRichEditOle.SetLinkAvailable
title: IRichEditOle::SetLinkAvailable
author: windows-sdk-content
description: Sets the value of the link-available bit in the object's flags.
old-location: controls\IRichEditOle_SetLinkAvailable.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditolesetlinkavailable.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IRichEditOle interface [Windows Controls],SetLinkAvailable method, IRichEditOle.SetLinkAvailable, IRichEditOle::SetLinkAvailable, SetLinkAvailable, SetLinkAvailable method [Windows Controls], SetLinkAvailable method [Windows Controls],IRichEditOle interface, _win32_IRichEditOle_SetLinkAvailable, _win32_IRichEditOle_SetLinkAvailable_cpp, controls.IRichEditOle_SetLinkAvailable, controls._win32_IRichEditOle_SetLinkAvailable, richole/IRichEditOle::SetLinkAvailable
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
 - IRichEditOle.SetLinkAvailable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRichEditOle::SetLinkAvailable


## -description


Sets the value of the link-available bit in the object's flags. The link-available bit defaults to <b>TRUE</b>. It should be set to <b>FALSE</b> if any errors occur on the link which would indicate problems connecting to the linked object or application. When those problems are repaired, the bit should be set to <b>TRUE</b> again.


## -parameters




### -param iob

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Index of object whose bit is to be set. If this parameter is REO_IOB_SELECTION, the bit on the selected object is to be set. 


### -param fAvailable

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Value used in the set operation. The value can be <b>TRUE</b> or <b>FALSE</b>. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK on success, or a failure code otherwise. E_INVALIDARG is returned if the index is invalid.




## -see-also




<a href="https://msdn.microsoft.com/d6d1794b-f16c-4a8c-84f5-dfe8bd8be08c">IRichEditOle</a>
 

 

