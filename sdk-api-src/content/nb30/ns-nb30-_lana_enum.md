---
UID: NS:nb30._LANA_ENUM
title: "_LANA_ENUM"
author: windows-sdk-content
description: The LANA_ENUM structure contains the numbers for the current LAN adapters.
old-location: netbios\lana_enum.htm
tech.root: NetBIOS
ms.assetid: 19a16eae-8c3e-4c4e-957b-41f22b61e51b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PLANA_ENUM, LANA_ENUM, LANA_ENUM structure [NetBIOS], PLANA_ENUM, PLANA_ENUM structure pointer [NetBIOS], _LANA_ENUM, nb30/LANA_ENUM, nb30/PLANA_ENUM, netbios.lana_enum"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: nb30.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Nb30.h
api_name:
 - LANA_ENUM
product: Windows
targetos: Windows
req.typenames: LANA_ENUM, *PLANA_ENUM
req.redist: 
---

# _LANA_ENUM structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/9144e283-0e5f-43d7-8cd2-e746f94c6f14">Netbios</a> is not supported on Windows Vista,  Windows Server 2008, and subsequent versions of the operating system]

The <b>LANA_ENUM</b> structure contains the numbers for the current LAN adapters.


## -struct-fields




### -field length

Specifies the number of valid entries in the array of LAN adapter numbers.


### -field lana

Specifies an array of LAN adapter numbers.


## -remarks



The <b>LANA_ENUM</b> structure is pointed to by the ncb_buffer member of the <a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a> structure when an application issues the <b>NCBENUM</b> command. The <b>NCBENUM</b> command is not part of the IBM NetBIOS 3.0 specification.




## -see-also




<b></b>



<a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a>



<a href="https://msdn.microsoft.com/64ef39ec-d69a-4e33-9192-dda6d1bb84b8">NetBIOS Structures</a>



<a href="https://msdn.microsoft.com/9144e283-0e5f-43d7-8cd2-e746f94c6f14">The NetBIOS Interface Overview</a>
 

 

