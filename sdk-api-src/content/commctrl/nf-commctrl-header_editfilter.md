---
UID: NF:commctrl.Header_EditFilter
title: Header_EditFilter macro
author: windows-sdk-content
description: Moves the input focus to the edit box when a filter button has the focus.
old-location: controls\Header_EditFilter.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\header\macros\header_editfilter.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: FALSE, Header_EditFilter, Header_EditFilter macro [Windows Controls], TRUE, _win32_Header_EditFilter, _win32_Header_EditFilter_cpp, commctrl/Header_EditFilter, controls.Header_EditFilter, controls._win32_Header_EditFilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
 - Header_EditFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Header_EditFilter macro


## -description


Moves the input focus to the edit box when a filter button has the focus.


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the header control. 


### -param i

Type: <b>int</b>

A value specifying the column to edit. 


### -param fDiscardChanges

Type: <b>fDiscardChanges</b>

A flag that specifies how to handle the user's editing changes. Use this flag to specify what to do if the user is in the process of editing the filter when the message is sent. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
Discard the changes made by the user. 

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Accept the changes made by the user. 

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775312(v=VS.85).aspx">HDM_EDITFILTER</a>
 

 

