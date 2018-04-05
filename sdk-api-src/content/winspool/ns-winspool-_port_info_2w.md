---
UID: NS:winspool._PORT_INFO_2W
title: "_PORT_INFO_2W"
author: windows-driver-content
description: The PORT_INFO_2 structure identifies a supported printer port.
old-location: gdi\port_info_2.htm
old-project: printdocs
ms.assetid: 93675294-61d4-40e4-b84c-f252978e0285
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*LPPORT_INFO_2W, *PPORT_INFO_2W, PORT_INFO_2, PORT_INFO_2 structure [Windows GDI], PORT_INFO_2W, PORT_TYPE_NET_ATTACHED, PORT_TYPE_READ, PORT_TYPE_REDIRECTED, PORT_TYPE_WRITE, PPORT_INFO_2, PPORT_INFO_2 structure pointer [Windows GDI], _PORT_INFO_2A, _PORT_INFO_2W, _win32_PORT_INFO_2_str, gdi.port_info_2, winspool/PORT_INFO_2, winspool/PPORT_INFO_2, winspool/_PORT_INFO_2A, winspool/_PORT_INFO_2W"
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
req.unicode-ansi: "_PORT_INFO_2W (Unicode) and _PORT_INFO_2A (ANSI)"
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PORT_INFO_2W, *PPORT_INFO_2W, *LPPORT_INFO_2W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PORT_INFO_2
-	_PORT_INFO_2A
-	_PORT_INFO_2W
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _PORT_INFO_2W structure


## -description



The <b>PORT_INFO_2</b> structure identifies a supported printer port.




## -struct-fields




### -field pPortName

Pointer to a null-terminated string that identifies a supported printer port (for example, "LPT1:").


### -field pMonitorName

Pointer to a null-terminated string that identifies an installed monitor (for example, "PJL monitor"). This can be <b>NULL</b>.


### -field pDescription

Pointer to a null-terminated string that describes the port in more detail (for example, if <b>pPortName</b> is "LPT1:", <b>pDescription</b> is "printer port"). This can be <b>NULL</b>.


### -field fPortType

Bitmask describing the type of port. This member can be a combination of the following values:

<a id="PORT_TYPE_WRITE"></a>
<a id="port_type_write"></a>


#### PORT_TYPE_WRITE

<a id="PORT_TYPE_READ"></a>
<a id="port_type_read"></a>


#### PORT_TYPE_READ

<a id="PORT_TYPE_REDIRECTED"></a>
<a id="port_type_redirected"></a>


#### PORT_TYPE_REDIRECTED

<a id="PORT_TYPE_NET_ATTACHED"></a>
<a id="port_type_net_attached"></a>


#### PORT_TYPE_NET_ATTACHED


### -field Reserved

Reserved; must be zero.


##### - fPortType.PORT_TYPE_NET_ATTACHED


##### - fPortType.PORT_TYPE_READ

<a id="PORT_TYPE_REDIRECTED"></a>
<a id="port_type_redirected"></a>

##### - fPortType.PORT_TYPE_REDIRECTED

<a id="PORT_TYPE_NET_ATTACHED"></a>
<a id="port_type_net_attached"></a>

##### - fPortType.PORT_TYPE_WRITE

<a id="PORT_TYPE_READ"></a>
<a id="port_type_read"></a>

## -remarks



Use the <b>PORT_INFO_2</b> structure when calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff548754">EnumPorts</a> if there are multiple monitors installed that support the same ports.


         The <b>fPortType</b> member can be queried to determine information about the port. Note that port settings do not influence printer attributes (as returned by the <b>Attributes</b> member of <a href="https://msdn.microsoft.com/944cbfcd-9edf-4b60-a45c-9bb1839f8141">PRINTER_INFO_2</a>).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff548754">EnumPorts</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

