---
UID: NF:termmgr.ITTerminalControl.ConnectTerminal
title: ITTerminalControl::ConnectTerminal
author: windows-sdk-content
description: The ConnectTerminal method connects filters and returns a set of pins for connection. Enters each of the internal filters into the filter graph, connects the internal filters together (if applicable) and returns a set of pins for connection.
old-location: tapi3\itterminalcontrol_connectterminal.htm
old-project: tapi
ms.assetid: 0351e645-b857-44d8-a226-046ebe0f4c81
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ConnectTerminal, ConnectTerminal method [TAPI 2.2], ConnectTerminal method [TAPI 2.2],ITTerminalControl interface, ITTerminalControl interface [TAPI 2.2],ConnectTerminal method, ITTerminalControl.ConnectTerminal, ITTerminalControl::ConnectTerminal, _tapi3_itterminalcontrol_connectterminal, tapi3.itterminalcontrol_connectterminal, termmgr/ITTerminalControl::ConnectTerminal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: termmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: TMGR_DIRECTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Termmgr.h
api_name:
 - ITTerminalControl.ConnectTerminal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTerminalControl::ConnectTerminal


## -description


The 
<b>ConnectTerminal</b> method connects filters and returns a set of pins for connection. Enters each of the internal filters into the filter graph, connects the internal filters together (if applicable) and returns a set of pins for connection.


## -parameters




### -param pGraph [in]

Pointer to graph builder interface.


### -param dwTerminalDirection [in]

Indicator of 
<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">terminal direction</a>.


### -param pdwNumPins [in, out]

Pointer to number of pins.


### -param ppPins [out]

Pointer to array of pins to be used for media transport related to the current terminal.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NOTENOUGHMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_TERMINALINUSE</b></dt>
</dl>
</td>
<td width="60%">
The current terminal is already in use.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6fe60002-3af3-45e9-a084-7296a48e7263">ITTerminalControl</a>
 

 

