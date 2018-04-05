---
UID: NS:ws2def.sockaddr_storage_xp
title: sockaddr_storage_xp
author: windows-driver-content
description: The SOCKADDR_STORAGE structure stores socket address information.
old-location: winsock\sockaddr_storage_2.htm
old-project: WinSock
ms.assetid: dfd84b91-0a94-4fe6-b8d2-18562afb9c24
ms.author: windowsdriverdev
ms.date: 3/30/2018
ms.keywords: "*LPSOCKADDR_STORAGE_XP, *PSOCKADDR_STORAGE, *PSOCKADDR_STORAGE_XP, PSOCKADDR_STORAGE, PSOCKADDR_STORAGE structure pointer [Winsock], SOCKADDR_STORAGE, SOCKADDR_STORAGE structure [Winsock], SOCKADDR_STORAGE_LH, SOCKADDR_STORAGE_XP, _win32_sockaddr_storage_2, sockaddr_storage_xp, winsock.sockaddr_storage_2, winsock2/PSOCKADDR_STORAGE, winsock2/SOCKADDR_STORAGE, ws2def/PSOCKADDR_STORAGE, ws2def/SOCKADDR_STORAGE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ws2def.h
req.include-header: Winsock2.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wrdsgraphicschannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SOCKADDR_STORAGE_XP, *PSOCKADDR_STORAGE_XP, *LPSOCKADDR_STORAGE_XP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ws2def.h
-	Winsock2.h
api_name:
-	SOCKADDR_STORAGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# sockaddr_storage_xp structure


## -description



			The 
<b>SOCKADDR_STORAGE</b> structure stores socket address information. Since the 
<b>SOCKADDR_STORAGE</b> structure is sufficiently large to store address information for IPv4, IPv6, or other  address families, its use promotes protocol-family and protocol-version independence and simplifies cross-platform development. Use the 
<b>SOCKADDR_STORAGE</b> structure in place of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure.


## -struct-fields




### -field ss_family

Address family of the socket, such as AF_INET. 

On Windows Vista
  and later, the datatype for this member is defined as an <b>ADDRESS_FAMILY</b>.


### -field __ss_pad1

Reserved. Defined as a 48-bit pad that ensures 
<b>SOCKADDR_STORAGE</b> achieves 64-bit alignment.


### -field __ss_align

Reserved. Used by the compiler to align the structure.


### -field __ss_pad2

Reserved. Used by the compiler to align the structure.


## -remarks



In the Microsoft Windows Software Development Kit (SDK), the version of this structure for use on Windows Vista
  and later is defined as <b>SOCKADDR_STORAGE_LH</b>. In the Windows SDK, the version of this structure to be used on earlier systems including Windows XP and later is defined as <b>SOCKADDR_STORAGE_XP</b>. When compiling an application if the target platform is Windows Vista and later (<b>NTDDI_VERSION &gt;= NTDDI_LONGHORN, _WIN32_WINNT &gt;= 0x0600</b>, or <b>WINVER &gt;= 0x0600</b>), the <b>SOCKADDR_STORAGE_LH</b> structure is typedefed to the <b>SOCKADDR_STORAGE</b> structure. When compiling an application if the target platform is not Windows Vista and later, the <b>SOCKADDR_STORAGE_XP</b> structure is typedefed to the <b>SOCKADDR_STORAGE</b> structure. 



The <b>SOCKADDR_STORAGE_LH</b> structure defines the data type of first member of the structure as an <b>ADDRESS_FAMILY</b>.

Application developers normally use only the <b>ss_family</b> member of the 
<b>SOCKADDR_STORAGE</b>. The remaining members ensure that the 
<b>SOCKADDR_STORAGE</b> can contain either an IPv6 or IPv4 address and the structure is padded appropriately to achieve 64-bit alignment. Such alignment enables protocol-specific socket address data structures to access fields within a 
<b>SOCKADDR_STORAGE</b> structure without alignment problems. With its padding, the 
<b>SOCKADDR_STORAGE</b> structure is 128 bytes in length.

The first member field of the 
<b>SOCKADDR_STORAGE</b> structure is isomorphic with the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a> structure to enable a simplified transition from 
the sockaddr structure to 
the <b>SOCKADDR_STORAGE</b> structure.

For more information about platform-independent 
<b>SOCKADDR_STORAGE</b> implementation recommendations, refer to RFC 2553, available at 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84023">www.ietf.org</a>.

On the Windows SDK released for Windows Vista and later, the organization of header files has changed and the <b>SOCKADDR_STORAGE</b> structure is defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff570822">sockaddr</a>
 

 

