---
UID: NS:winuser.tagCOPYDATASTRUCT
title: COPYDATASTRUCT (winuser.h)
description: Contains data to be passed to another application by the WM_COPYDATA message.helpviewer_keywords: ["*PCOPYDATASTRUCT","COPYDATASTRUCT","COPYDATASTRUCT structure [Data Exchange]","PCOPYDATASTRUCT","PCOPYDATASTRUCT structure pointer [Data Exchange]","_win32_COPYDATASTRUCT_str","_win32_copydatastruct_str_cpp","dataxchg.copydatastruct","winui._win32_copydatastruct_str","winuser/COPYDATASTRUCT","winuser/PCOPYDATASTRUCT"]
old-location: dataxchg\copydatastruct.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\datacopy\datacopyreference\datacopystructures\copydatastruct.htm
ms.date: 12/05/2018
ms.keywords: '*PCOPYDATASTRUCT, COPYDATASTRUCT, COPYDATASTRUCT structure [Data Exchange], PCOPYDATASTRUCT, PCOPYDATASTRUCT structure pointer [Data Exchange], _win32_COPYDATASTRUCT_str, _win32_copydatastruct_str_cpp, dataxchg.copydatastruct, winui._win32_copydatastruct_str, winuser/COPYDATASTRUCT, winuser/PCOPYDATASTRUCT'
f1_keywords:
- winuser/COPYDATASTRUCT
dev_langs:
- c++
req.header: winuser.h
req.include-header: Windows.h
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
- Winuser.h
api_name:
- COPYDATASTRUCT
targetos: Windows
req.typenames: COPYDATASTRUCT, *PCOPYDATASTRUCT
req.redist: 
ms.custom: 19H1
---

# COPYDATASTRUCT structure


## -description


Contains data to be passed to another application by the <a href="https://docs.microsoft.com/windows/desktop/dataxchg/wm-copydata">WM_COPYDATA</a> message. 


## -struct-fields




### -field dwData

Type: <b>ULONG_PTR</b>

The data to be passed to the receiving application. 


### -field cbData

Type: <b>DWORD</b>

The size, in bytes, of the data pointed to by the <b>lpData</b> member. 


### -field lpData

Type: <b>PVOID</b>

The data to be passed to the receiving application. This member can be <b>NULL</b>. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dataxchg/wm-copydata">WM_COPYDATA</a>
 

 

