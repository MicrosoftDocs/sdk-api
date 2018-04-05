---
UID: NS:winspool._PORT_INFO_3W
title: "_PORT_INFO_3W"
author: windows-driver-content
description: The PORT_INFO_3 structure specifies the status value of a printer port.
old-location: gdi\port_info_3.htm
old-project: printdocs
ms.assetid: 0939353f-284b-4dbb-89a2-04918c934430
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPORT_INFO_3W, *PPORT_INFO_3W, PORT_INFO_3, PORT_INFO_3 structure [Windows GDI], PORT_INFO_3W, PPORT_INFO_3, PPORT_INFO_3 structure pointer [Windows GDI], _PORT_INFO_3A, _PORT_INFO_3W, _win32_PORT_INFO_3_str, gdi.port_info_3, winspool/PORT_INFO_3, winspool/PPORT_INFO_3, winspool/_PORT_INFO_3A, winspool/_PORT_INFO_3W"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: "_PORT_INFO_3W (Unicode) and _PORT_INFO_3A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PORT_INFO_3W, *PPORT_INFO_3W, *LPPORT_INFO_3W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PORT_INFO_3
-	_PORT_INFO_3A
-	_PORT_INFO_3W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PORT_INFO_3W structure


## -description



The <b>PORT_INFO_3</b> structure specifies the status value of a printer port.




## -struct-fields




### -field dwStatus

The new port status value. This value is used only if the <b>pszStatus</b> member is <b>NULL</b>.

This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>0</td>
<td>Clears the printer port status.</td>
</tr>
<tr>
<td>PORT_STATUS_OFFLINE</td>
<td>The port's printer is offline.</td>
</tr>
<tr>
<td>PORT_STATUS_PAPER_JAM</td>
<td>The port's printer has a paper jam.</td>
</tr>
<tr>
<td>PORT_STATUS_PAPER_OUT</td>
<td>The port's printer is out of paper.</td>
</tr>
<tr>
<td>PORT_STATUS_OUTPUT_BIN_FULL</td>
<td>The port's printer's output bin is full.</td>
</tr>
<tr>
<td>PORT_STATUS_PAPER_PROBLEM</td>
<td>The port's printer has a paper problem.</td>
</tr>
<tr>
<td>PORT_STATUS_NO_TONER</td>
<td>The port's printer is out of toner.</td>
</tr>
<tr>
<td>PORT_STATUS_DOOR_OPEN</td>
<td>The door of the port's printer is open.</td>
</tr>
<tr>
<td>PORT_STATUS_USER_INTERVENTION</td>
<td>The port's printer requires user intervention.</td>
</tr>
<tr>
<td>PORT_STATUS_OUT_OF_MEMORY</td>
<td>The port's printer is out of memory.</td>
</tr>
<tr>
<td>PORT_STATUS_TONER_LOW</td>
<td>The port's printer is low on toner.</td>
</tr>
<tr>
<td>PORT_STATUS_WARMING_UP</td>
<td>The port's printer is warming up.</td>
</tr>
<tr>
<td>PORT_STATUS_POWER_SAVE</td>
<td>The port's printer is in a power-conservation mode.</td>
</tr>
</table>
 


### -field pszStatus

Pointer to a new printer port status value string to set. Use this member if there is no suitable status value among those listed for <b>dwStatus</b>.


### -field dwSeverity

The severity of the port status value.

This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PORT_STATUS_TYPE_ERROR</td>
<td>The port status value indicates an error.</td>
</tr>
<tr>
<td>PORT_STATUS_TYPE_WARNING</td>
<td>The port status value is a warning.</td>
</tr>
<tr>
<td>PORT_STATUS_TYPE_INFO</td>
<td>The port status value is informational.</td>
</tr>
</table>
 


## -remarks



When you set a printer port status value with the severity value PORT_STATUS_TYPE_ERROR, the print spooler stops sending jobs to the port. The print spooler does not resume sending jobs to the port until another <a href="https://msdn.microsoft.com/1b80ad93-aaa1-41ed-a668-a944fa62c3eb">SetPort</a> call is made to clear the status.




## -see-also




<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/1b80ad93-aaa1-41ed-a668-a944fa62c3eb">SetPort</a>
 

 

