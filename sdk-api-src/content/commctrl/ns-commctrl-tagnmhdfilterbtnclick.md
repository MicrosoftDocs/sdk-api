---
UID: NS:commctrl.tagNMHDFILTERBTNCLICK
title: tagNMHDFILTERBTNCLICK
author: windows-sdk-content
description: Specifies or receives the attributes of a filter button click.
old-location: controls\NMHDFILTERBTNCLICK.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\header\structures\nmhdfilterbtnclick.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*LPNMHDFILTERBTNCLICK, LPNMHDFILTERBTNCLICK, LPNMHDFILTERBTNCLICK structure pointer [Windows Controls], NMHDFILTERBTNCLICK, NMHDFILTERBTNCLICK structure [Windows Controls], _win32_NMHDFILTERBTNCLICK_Structure, _win32_NMHDFILTERBTNCLICK_Structure_cpp, commctrl/LPNMHDFILTERBTNCLICK, commctrl/NMHDFILTERBTNCLICK, controls.NMHDFILTERBTNCLICK, controls._win32_NMHDFILTERBTNCLICK_Structure, tagNMHDFILTERBTNCLICK"
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
 - NMHDFILTERBTNCLICK
product: Windows
targetos: Windows
req.typenames: NMHDFILTERBTNCLICK, *LPNMHDFILTERBTNCLICK
req.redist: 
---

# tagNMHDFILTERBTNCLICK structure


## -description


Specifies or receives the attributes of a filter button click. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>

A handle of an <a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains additional information. 


### -field iItem

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

The zero-based index of the control to which this structure refers. 


### -field rc

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the client rectangle for the filter button. 


## -see-also




<a href="https://msdn.microsoft.com/36b85cdc-1022-4568-8891-0c919c850fd4">HDN_FILTERBTNCLICK</a>
 

 

