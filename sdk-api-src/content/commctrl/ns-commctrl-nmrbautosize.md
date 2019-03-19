---
UID: NS:commctrl.tagNMRBAUTOSIZE
title: NMRBAUTOSIZE (commctrl.h)
author: windows-sdk-content
description: Contains information used in handling the RBN_AUTOSIZE notification codes.
old-location: controls\NMRBAUTOSIZE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\rebar\structures\nmrbautosize.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPNMRBAUTOSIZE, LPNMRBAUTOSIZE, LPNMRBAUTOSIZE structure pointer [Windows Controls], NMRBAUTOSIZE, NMRBAUTOSIZE structure [Windows Controls], _win32_NMRBAUTOSIZE, _win32_NMRBAUTOSIZE_cpp, commctrl/LPNMRBAUTOSIZE, commctrl/NMRBAUTOSIZE, controls.NMRBAUTOSIZE, controls._win32_NMRBAUTOSIZE"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - NMRBAUTOSIZE
product: Windows
targetos: Windows
req.typenames: NMRBAUTOSIZE, *LPNMRBAUTOSIZE
req.redist: 
---

# NMRBAUTOSIZE structure


## -description


Contains information used in handling the <a href="https://msdn.microsoft.com/en-us/library/Bb774405(v=VS.85).aspx">RBN_AUTOSIZE</a> notification codes. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains additional information about the notification. 


### -field fChanged

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Member that indicates if the size or layout of the rebar control has changed (nonzero if a change occurred or zero otherwise). 


### -field rcTarget

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>


<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the rectangle to which the rebar control tried to size itself. 


### -field rcActual

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>


<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the rectangle to which the rebar control actually sized itself. 

