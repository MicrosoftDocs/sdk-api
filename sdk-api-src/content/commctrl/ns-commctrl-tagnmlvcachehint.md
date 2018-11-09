---
UID: NS:commctrl.tagNMLVCACHEHINT
title: tagNMLVCACHEHINT
author: windows-sdk-content
description: Contains information used to update the cached item information for use with a virtual list view.
old-location: controls\NMLVCACHEHINT.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvcachehint.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPNMLVCACHEHINT, NMLVCACHEHINT, NMLVCACHEHINT structure [Windows Controls], PNMLVCACHEHINT, PNMLVCACHEHINT structure pointer [Windows Controls], _win32_NMLVCACHEHINT, _win32_NMLVCACHEHINT_cpp, commctrl/NMLVCACHEHINT, commctrl/PNMLVCACHEHINT, controls.NMLVCACHEHINT, controls._win32_NMLVCACHEHINT, tagNMLVCACHEHINT"
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
 - NMLVCACHEHINT
product: Windows
targetos: Windows
req.typenames: NMLVCACHEHINT, *LPNMLVCACHEHINT
req.redist: 
---

# tagNMLVCACHEHINT structure


## -description


Contains information used to update the cached item information for use with a <a href="https://msdn.microsoft.com/en-us/library/Bb774735(v=VS.85).aspx">virtual list view</a>. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains information about this notification message. 


### -field iFrom

Type: <b>int</b>

Starting index of the requested range of items. This value is inclusive. 


### -field iTo

Type: <b>int</b>

Ending index of the requested range of items. This value is inclusive. 

