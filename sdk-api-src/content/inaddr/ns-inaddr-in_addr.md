---
UID: NS:inaddr.in_addr
title: in_addr
author: windows-sdk-content
description: The in_addr structure represents an IPv4 address.
old-location: iphlp\ipaddr.htm
old-project: iphlp
ms.assetid: 00d4823d-114d-4cc7-afdf-54c7fed3fe45
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*LPIN_ADDR, *PIN_ADDR, IN_ADDR, IPAddr, IPAddr structure [IP Helper], in_addr, in_addr structure [IP Helper], inaddr/in_addr, ipexport/in_addr, iphlp.ipaddr"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: inaddr.h
req.include-header: Ipexport.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: IN_ADDR, *PIN_ADDR, *LPIN_ADDR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Inaddr.h
 - Ipexport.h
api_name:
 - IPAddr
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# in_addr structure


## -description


The <b>in_addr</b> structure represents an IPv4 address.
<div class="alert"><b>Note</b>  The <b>IPaddr</b> type definition in IP Helper also represents an IPv4 address and can be cast to an interchangeable <a href="https://msdn.microsoft.com/library/windows/hardware/ff556972">in_addr</a> structure when needed. The <b>in_addr</b> structure in IP Helper has the same syntax and usage as the Windows Sockets <b>in_addr</b> structure, and is interchangeable with <b>in_addr</b> structure used in Windows sockets. Windows sockets also defines an <b>IN_ADDR</b> typedef for the <b>in_addr</b> structure.</div><div> </div>

## -struct-fields




### -field S_un


### -field S_un.S_un_b

The IPv4 address of the host formatted as four <b>u_char</b>s.


### -field S_un.S_un_b.s_b1

 


### -field S_un.S_un_b.s_b2

 


### -field S_un.S_un_b.s_b3

 


### -field S_un.S_un_b.s_b4

 


### -field S_un.S_un_w

The IPv4 address of the host formatted as two <b>u_short</b>s.


### -field S_un.S_un_w.s_w1

 


### -field S_un.S_un_w.s_w2

 


### -field S_un.S_addr

Address of the host formatted as a <b>u_long</b>.


## -remarks



The <b>IPaddr</b> type definition also represents an IPv4 address and can be cast to an  <b>in_addr</b> structure when needed.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>in_addr</b> structure is defined in the <i>Inaddr.h</i> header file which is automatically included by the <i>Ipexport.h</i> header file. On the Platform Software Development Kit (SDK) released for Windows Server 2003 and Windows XP, the <b>in_addr</b> structure is declared in the <i>Ipexport.h</i> header file. 




## -see-also




<a href="https://msdn.microsoft.com/6495d289-b9b8-42cb-b00b-cde53d3dc91c">ARP_SEND_REPLY</a>



<a href="https://msdn.microsoft.com/669264cd-a43c-4681-9416-2704d4232685">AddIPAddress</a>



<a href="https://msdn.microsoft.com/9171cdf7-4057-4a8d-a34c-1b7b1f94bcb1">GetBestInterface</a>



<a href="https://msdn.microsoft.com/4e84fe6f-40bd-4f0e-bb78-4180e13577aa">GetRTTAndHopCount</a>



<a href="https://msdn.microsoft.com/e6d43c35-1009-4df1-bc39-aec97178cae6">ICMP_ECHO_REPLY</a>



<a href="https://msdn.microsoft.com/225b93ae-e34f-4e5b-a699-1fdd342265c6">IP_UNIDIRECTIONAL_ADAPTER_ADDRESS</a>



<a href="https://msdn.microsoft.com/c3cdc535-2c13-48c6-9ab1-88cc5e5119b5">IcmpSendEcho</a>



<a href="https://msdn.microsoft.com/1f70b6cc-9085-4eb8-b2cc-3b3d98d0ea46">IcmpSendEcho2</a>



<a href="https://msdn.microsoft.com/5cbaf45a-a64e-49fd-a920-01759b5c4f81">SendARP</a>



<a href="https://msdn.microsoft.com/fc41a2d1-ea6e-41bb-b2c8-531ac8b5434c">in_addr(Winsock)</a>
 

 

