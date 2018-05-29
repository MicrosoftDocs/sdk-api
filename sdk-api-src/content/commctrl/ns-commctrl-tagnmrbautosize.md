---
UID: NS:commctrl.tagNMRBAUTOSIZE
title: tagNMRBAUTOSIZE
author: windows-sdk-content
description: Contains information used in handling the RBN_AUTOSIZE notification codes.
old-location: controls\NMRBAUTOSIZE.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\rebar\structures\nmrbautosize.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*LPNMRBAUTOSIZE, LPNMRBAUTOSIZE, LPNMRBAUTOSIZE structure pointer [Windows Controls], NMRBAUTOSIZE, NMRBAUTOSIZE structure [Windows Controls], _win32_NMRBAUTOSIZE, _win32_NMRBAUTOSIZE_cpp, commctrl/LPNMRBAUTOSIZE, commctrl/NMRBAUTOSIZE, controls.NMRBAUTOSIZE, controls._win32_NMRBAUTOSIZE, tagNMRBAUTOSIZE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commctrl.h
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
req.typenames: NMRBAUTOSIZE, *LPNMRBAUTOSIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	NMRBAUTOSIZE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagNMRBAUTOSIZE structure


## -description


Contains information used in handling the <a href="https://msdn.microsoft.com/d174fe99-13cc-404c-9dc5-d5a93e9807a2">RBN_AUTOSIZE</a> notification codes. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains additional information about the notification. 


### -field fChanged

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Member that indicates if the size or layout of the rebar control has changed (nonzero if a change occurred or zero otherwise). 


### -field rcTarget

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>


<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the rectangle to which the rebar control tried to size itself. 


### -field rcActual

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>


<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the rectangle to which the rebar control actually sized itself. 

