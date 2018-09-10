---
UID: NF:commctrl.UninitializeFlatSB
title: UninitializeFlatSB function
author: windows-sdk-content
description: Uninitializes flat scroll bars for a particular window. The specified window will revert to standard scroll bars.
old-location: controls\UninitializeFlatSB.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\flatsb\functions\uninitializeflatsb.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: UninitializeFlatSB, UninitializeFlatSB function [Windows Controls], _win32_UninitializeFlatSB, _win32_UninitializeFlatSB_cpp, commctrl/UninitializeFlatSB, controls.UninitializeFlatSB, controls._win32_UninitializeFlatSB
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - UninitializeFlatSB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UninitializeFlatSB function


## -description


Uninitializes flat scroll bars for a particular window. The specified window will revert to standard scroll bars. 


## -parameters




### -param Arg1

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the window with the flat scroll bars that will be uninitialized. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns one of the following values. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
One of the window's scroll bars is currently in use. The operation cannot be completed at this time. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The window does not have flat scroll bars initialized. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful. 

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  Flat scroll bar functions are implemented in Comctl32.dll versions 4.71 through 5.82. Comctl32.dll versions 6.00 and higher do not support flat scroll bars.</div>
<div> </div>


