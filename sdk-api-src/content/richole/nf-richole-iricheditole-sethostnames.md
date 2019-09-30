---
UID: NF:richole.IRichEditOle.SetHostNames
title: IRichEditOle::SetHostNames (richole.h)
author: windows-sdk-content
description: Sets the host names to be given to objects as they are inserted to a rich edit control. The host names are used in the user interface of servers to describe the container context of opened objects.
old-location: controls\IRichEditOle_SetHostNames.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditolesethostnames.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRichEditOle interface [Windows Controls],SetHostNames method, IRichEditOle.SetHostNames, IRichEditOle::SetHostNames, SetHostNames, SetHostNames method [Windows Controls], SetHostNames method [Windows Controls],IRichEditOle interface, _win32_IRichEditOle_SetHostNames, _win32_IRichEditOle_SetHostNames_cpp, controls.IRichEditOle_SetHostNames, controls._win32_IRichEditOle_SetHostNames, richole/IRichEditOle::SetHostNames
ms.topic: method
f1_keywords: 
 - "richole/IRichEditOle.SetHostNames"
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
 - IRichEditOle.SetHostNames
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRichEditOle::SetHostNames


## -description


Sets the host names to be given to objects as they are inserted to a rich edit control. The host names are used in the user interface of servers to describe the container context of opened objects.


## -parameters




### -param lpstrContainerApp

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

Null-terminated name of the container application. 


### -param lpstrContainerObj

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

Null-terminated name of the container document or object. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK on success, or a failure code otherwise. E_OUTOFMEMORY is returned if memory could not be allocated to remember the strings.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/richole/nn-richole-iricheditole">IRichEditOle</a>
 

 

