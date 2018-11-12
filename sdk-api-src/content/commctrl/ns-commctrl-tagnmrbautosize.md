---
UID: NS:commctrl.tagNMRBAUTOSIZE
title: tagNMRBAUTOSIZE
author: windows-sdk-content
description: Contains information used in handling the RBN_AUTOSIZE notification codes.
old-location: controls\NMRBAUTOSIZE.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\rebar\structures\nmrbautosize.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
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

# tagNMRBAUTOSIZE structure


## -description


Contains information used in handling the <a href="https://msdn.microsoft.com/en-us/library/Bb774405(v=VS.85).aspx">RBN_AUTOSIZE</a> notification codes. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains additional information about the notification. 


### -field fChanged

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

Member that indicates if the size or layout of the rebar control has changed (nonzero if a change occurred or zero otherwise). 


### -field rcTarget

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>


<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the rectangle to which the rebar control tried to size itself. 


### -field rcActual

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>


<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the rectangle to which the rebar control actually sized itself. 

