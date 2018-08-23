---
UID: NS:commctrl.tagNMHDFILTERBTNCLICK
title: tagNMHDFILTERBTNCLICK
author: windows-sdk-content
description: Specifies or receives the attributes of a filter button click.
old-location: controls\NMHDFILTERBTNCLICK.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\header\structures\nmhdfilterbtnclick.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPNMHDFILTERBTNCLICK, LPNMHDFILTERBTNCLICK, LPNMHDFILTERBTNCLICK structure pointer [Windows Controls], NMHDFILTERBTNCLICK, NMHDFILTERBTNCLICK structure [Windows Controls], _win32_NMHDFILTERBTNCLICK_Structure, _win32_NMHDFILTERBTNCLICK_Structure_cpp, commctrl/LPNMHDFILTERBTNCLICK, commctrl/NMHDFILTERBTNCLICK, controls.NMHDFILTERBTNCLICK, controls._win32_NMHDFILTERBTNCLICK_Structure, tagNMHDFILTERBTNCLICK"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: commctrl.h
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
req.typenames: NMHDFILTERBTNCLICK, *LPNMHDFILTERBTNCLICK
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
req.lib: 
req.dll: 
req.irql: 
---

# tagNMHDFILTERBTNCLICK structure


## -description


Specifies or receives the attributes of a filter button click. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>

A handle of an <a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> structure that contains additional information. 


### -field iItem

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">INT</a></b>

The zero-based index of the control to which this structure refers. 


### -field rc

Type: <b><a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a></b>

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the client rectangle for the filter button. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775275(v=VS.85).aspx">HDN_FILTERBTNCLICK</a>
 

 

