---
UID: NF:richole.IRichEditOle.HandsOffStorage
title: IRichEditOle::HandsOffStorage
author: windows-sdk-content
description: Indicates when a rich edit control is to release its reference to the storage interface associated with the specified object. This call does not call the object's IRichEditOle::HandsOffStorage method; the caller must do that.
old-location: controls\IRichEditOle_HandsOffStorage.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditolehandsoffstorage.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: HandsOffStorage, HandsOffStorage method [Windows Controls], HandsOffStorage method [Windows Controls],IRichEditOle interface, IRichEditOle interface [Windows Controls],HandsOffStorage method, IRichEditOle.HandsOffStorage, IRichEditOle::HandsOffStorage, _win32_IRichEditOle_HandsOffStorage, _win32_IRichEditOle_HandsOffStorage_cpp, controls.IRichEditOle_HandsOffStorage, controls._win32_IRichEditOle_HandsOffStorage, richole/IRichEditOle::HandsOffStorage
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
 - IRichEditOle.HandsOffStorage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRichEditOle::HandsOffStorage


## -description


Indicates when a rich edit control is to release its reference to the storage interface associated with the specified object. This call does not call the object's <b>IRichEditOle::HandsOffStorage</b> method; the caller must do that.


## -parameters




### -param iob

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Index of the object whose storage is to be released. If this parameter is REO_IOB_SELECTION, the storage of the selected object is to be released. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK on success, or a failure code otherwise. E_INVALIDARG is returned if the index is invalid.




## -see-also




<a href="https://msdn.microsoft.com/d6d1794b-f16c-4a8c-84f5-dfe8bd8be08c">IRichEditOle</a>
 

 

