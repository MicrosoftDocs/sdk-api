---
UID: NS:commctrl.TBINSERTMARK
title: TBINSERTMARK
author: windows-sdk-content
description: Contains information on the insertion mark in a toolbar control.
old-location: controls\TBINSERTMARK.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\tbinsertmark.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: "*LPTBINSERTMARK, 0, LPTBINSERTMARK, LPTBINSERTMARK structure pointer [Windows Controls], TBIMHT_AFTER, TBIMHT_BACKGROUND, TBINSERTMARK, TBINSERTMARK structure [Windows Controls], _win32_TBINSERTMARK, _win32_TBINSERTMARK_cpp, commctrl/LPTBINSERTMARK, commctrl/TBINSERTMARK, controls.TBINSERTMARK, controls._win32_TBINSERTMARK"
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
req.typenames: TBINSERTMARK, *LPTBINSERTMARK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	TBINSERTMARK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TBINSERTMARK structure


## -description


Contains information on the insertion mark in a toolbar control. 


## -struct-fields




### -field iButton

Type: <b>int</b>

Zero-based index of the insertion mark. If this member is -1, there is no insertion mark. 


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Defines where the insertion mark is in relation to 
					<b>iButton</b>. This can be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The insertion mark is to the left of the specified button. 

</td>
</tr>
<tr>
<td width="40%"><a id="TBIMHT_AFTER"></a><a id="tbimht_after"></a><dl>
<dt><b>TBIMHT_AFTER</b></dt>
</dl>
</td>
<td width="60%">
The insertion mark is to the right of the specified button. 

</td>
</tr>
<tr>
<td width="40%"><a id="TBIMHT_BACKGROUND"></a><a id="tbimht_background"></a><dl>
<dt><b>TBIMHT_BACKGROUND</b></dt>
</dl>
</td>
<td width="60%">
The insertion mark is on the background of the toolbar. This flag is only used with the <a href="https://msdn.microsoft.com/65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e">TB_INSERTMARKHITTEST</a> message. 

</td>
</tr>
</table>
 

