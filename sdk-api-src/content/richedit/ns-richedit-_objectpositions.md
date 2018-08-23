---
UID: NS:richedit._objectpositions
title: "_objectpositions"
author: windows-sdk-content
description: Contains object position information.
old-location: controls\OBJECTPOSITIONS.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\objectpositions.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: OBJECTPOSITIONS, OBJECTPOSITIONS structure [Windows Controls], _objectpositions, _win32_OBJECTPOSITIONS_str, _win32_OBJECTPOSITIONS_str_cpp, controls.OBJECTPOSITIONS, controls._win32_OBJECTPOSITIONS_str, richedit/OBJECTPOSITIONS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: richedit.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: OBJECTPOSITIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - OBJECTPOSITIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _objectpositions structure


## -description


Contains object position information. 


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

The <b>code</b> member of this structure identifies the notification code being sent. 


### -field cObjectCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Number of object positions.


### -field pcpPositions

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a>*</b>

The object positions. 


## -remarks



This is used in the <a href="https://msdn.microsoft.com/1965185f-8a13-4989-8574-af8b9b30f6b0">EN_OBJECTPOSITIONS</a> notification. 




## -see-also




<a href="https://msdn.microsoft.com/1965185f-8a13-4989-8574-af8b9b30f6b0">EN_OBJECTPOSITIONS</a>



<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a>



<b>Reference</b>
 

 

