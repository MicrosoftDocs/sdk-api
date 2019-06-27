---
UID: NF:richole.IRichEditOle.SaveCompleted
title: IRichEditOle::SaveCompleted (richole.h)
author: windows-sdk-content
description: Indicates when the most recent save operation has been completed and that the rich edit control should hold onto a different storage for the object.
old-location: controls\IRichEditOle_SaveCompleted.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditolesavecompleted.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRichEditOle interface [Windows Controls],SaveCompleted method, IRichEditOle.SaveCompleted, IRichEditOle::SaveCompleted, SaveCompleted, SaveCompleted method [Windows Controls], SaveCompleted method [Windows Controls],IRichEditOle interface, _win32_IRichEditOle_SaveCompleted, _win32_IRichEditOle_SaveCompleted_cpp, controls.IRichEditOle_SaveCompleted, controls._win32_IRichEditOle_SaveCompleted, richole/IRichEditOle::SaveCompleted
ms.topic: method
f1_keywords: 
 - "richole/IRichEditOle.SaveCompleted"
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
 - IRichEditOle.SaveCompleted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRichEditOle::SaveCompleted


## -description


Indicates when the most recent save operation has been completed and that the rich edit control should hold onto a different storage for the object.


## -parameters




### -param iob

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Index of the object whose storage is being specified. If this parameter is REO_IOB_SELECTION, the selected object is used. 


### -param lpstg

Type: <b>LPSTORAGE</b>

New storage for the object. If the storage is not <b>NULL</b>, the rich edit control releases any storage it is currently holding for the object and uses this new storage instead. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK on success, or a failure code otherwise. E_INVALIDARG is returned if the index is invalid.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/richole/nn-richole-iricheditole">IRichEditOle</a>
 

 

