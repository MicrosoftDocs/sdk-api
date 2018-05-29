---
UID: NS:nb30._NAME_BUFFER
title: "_NAME_BUFFER"
author: windows-sdk-content
description: The NAME_BUFFER structure contains information about a local network name. One or more NAME_BUFFER structures follows an ADAPTER_STATUS structure when an application specifies the NCBASTAT command in the ncb_command member of the NCB structure.
old-location: netbios\name_buffer.htm
old-project: NetBIOS
ms.assetid: f1059074-68c1-4a08-98bd-ccfb314e39ec
ms.author: windowssdkdev
ms.date: 05/02/2018
ms.keywords: "*PNAME_BUFFER, DEREGISTERED, DUPLICATE, DUPLICATE_DEREG, GROUP_NAME, NAME_BUFFER, NAME_BUFFER structure [NetBIOS], PNAME_BUFFER, PNAME_BUFFER structure pointer [NetBIOS], REGISTERED, REGISTERING, UNIQUE_NAME, _NAME_BUFFER, nb30/NAME_BUFFER, nb30/PNAME_BUFFER, netbios.name_buffer"
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
req.typenames: NAME_BUFFER, *PNAME_BUFFER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Nb30.h
api_name:
-	NAME_BUFFER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _NAME_BUFFER structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/library/windows/hardware/dn965731">Netbios</a> is not supported on Windows Vista,  Windows Server 2008, and subsequent versions of the operating system]

The <b>NAME_BUFFER</b> structure contains information about a local network name. One or more <b>NAME_BUFFER</b> structures follows an <a href="https://msdn.microsoft.com/402bc5ce-bce4-4ba9-b82d-13cd3dc7097b">ADAPTER_STATUS</a> structure when an application specifies the <b>NCBASTAT</b> command in the ncb_command member of the <a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a> structure. 




## -struct-fields




### -field name

Specifies the local network name. This value is in the <b>ncb_name</b> member of the <a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a> structure.


### -field name_num

Specifies the number for the local network name. This value is in the <b>ncb_num</b> member of the <a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a> structure.


### -field name_flags

Specifies the current state of the name table entry. This member can be one of the following values.



##### )



##### )



###### )



##### )



##### )



##### )



##### )


## -see-also




<b></b>



<a href="https://msdn.microsoft.com/402bc5ce-bce4-4ba9-b82d-13cd3dc7097b">ADAPTER_STATUS</a>



<a href="https://msdn.microsoft.com/e3fcca1c-8057-41c4-80a5-d1e67920d88c">NCB</a>



<a href="https://msdn.microsoft.com/64ef39ec-d69a-4e33-9192-dda6d1bb84b8">NetBIOS Structures</a>



<a href="https://msdn.microsoft.com/9144e283-0e5f-43d7-8cd2-e746f94c6f14">The NetBIOS Interface Overview</a>
 

 

