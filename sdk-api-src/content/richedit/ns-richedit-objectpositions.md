---
UID: NS:richedit._objectpositions
title: OBJECTPOSITIONS (richedit.h)
description: Contains object position information.
helpviewer_keywords: ["OBJECTPOSITIONS","OBJECTPOSITIONS structure [Windows Controls]","_win32_OBJECTPOSITIONS_str","_win32_OBJECTPOSITIONS_str_cpp","controls.OBJECTPOSITIONS","controls._win32_OBJECTPOSITIONS_str","richedit/OBJECTPOSITIONS"]
old-location: controls\OBJECTPOSITIONS.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\objectpositions.htm
ms.date: 12/05/2018
ms.keywords: OBJECTPOSITIONS, OBJECTPOSITIONS structure [Windows Controls], _win32_OBJECTPOSITIONS_str, _win32_OBJECTPOSITIONS_str_cpp, controls.OBJECTPOSITIONS, controls._win32_OBJECTPOSITIONS_str, richedit/OBJECTPOSITIONS
f1_keywords:
- richedit/OBJECTPOSITIONS
dev_langs:
- c++
req.header: richedit.h
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Richedit.h
api_name:
- OBJECTPOSITIONS
targetos: Windows
req.typenames: OBJECTPOSITIONS
req.redist: 
ms.custom: 19H1
---

# OBJECTPOSITIONS structure


## -description


Contains object position information. 


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

The <b>code</b> member of this structure identifies the notification code being sent. 


### -field cObjectCount

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Number of object positions.


### -field pcpPositions

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LONG</a>*</b>

The object positions. 


## -remarks



This is used in the <a href="https://msdn.microsoft.com/1965185f-8a13-4989-8574-af8b9b30f6b0">EN_OBJECTPOSITIONS</a> notification. 




## -see-also




<a href="https://msdn.microsoft.com/1965185f-8a13-4989-8574-af8b9b30f6b0">EN_OBJECTPOSITIONS</a>



<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a>



<b>Reference</b>
 

 

