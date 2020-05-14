---
UID: NF:vfw.capSetUserData
title: capSetUserData macro (vfw.h)
description: The capSetUserData macro associates a LONG_PTR data value with a capture window. You can use this macro or explicitly call the WM_CAP_SET_USER_DATA message.helpviewer_keywords: ["_win32_capSetUserData","capSetUserData","capSetUserData macro [Windows Multimedia]","multimedia.capsetuserdata","vfw/capSetUserData"]
old-location: multimedia\capsetuserdata.htm
tech.root: Multimedia
ms.assetid: fefbef56-aedb-4158-9514-d19e7986d850
ms.date: 12/05/2018
ms.keywords: _win32_capSetUserData, capSetUserData, capSetUserData macro [Windows Multimedia], multimedia.capsetuserdata, vfw/capSetUserData
f1_keywords:
- vfw/capSetUserData
dev_langs:
- c++
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
- capSetUserData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# capSetUserData macro


## -description



The <b>capSetUserData</b> macro associates a <b>LONG_PTR</b> data value with a capture window. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/wm-cap-set-user-data">WM_CAP_SET_USER_DATA</a> message.




## -parameters




### -param hwnd

Handle to a capture window.


### -param lUser

Data value to associate with a capture window.


## -remarks



Typically this message is used to point to a block of data associated with a capture window.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture">Video Capture</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-capture-macros">Video Capture Macros</a>
 

 

