---
UID: NS:nb30._NAME_BUFFER
title: NAME_BUFFER (nb30.h)
description: The NAME_BUFFER structure contains information about a local network name. One or more NAME_BUFFER structures follows an ADAPTER_STATUS structure when an application specifies the NCBASTAT command in the ncb_command member of the NCB structure.
helpviewer_keywords: ["*PNAME_BUFFER","DEREGISTERED","DUPLICATE","DUPLICATE_DEREG","GROUP_NAME","NAME_BUFFER","NAME_BUFFER structure [NetBIOS]","PNAME_BUFFER","PNAME_BUFFER structure pointer [NetBIOS]","REGISTERED","REGISTERING","UNIQUE_NAME","nb30/NAME_BUFFER","nb30/PNAME_BUFFER","netbios.name_buffer"]
old-location: netbios\name_buffer.htm
tech.root: NetBIOS
ms.assetid: f1059074-68c1-4a08-98bd-ccfb314e39ec
ms.date: 12/05/2018
ms.keywords: '*PNAME_BUFFER, DEREGISTERED, DUPLICATE, DUPLICATE_DEREG, GROUP_NAME, NAME_BUFFER, NAME_BUFFER structure [NetBIOS], PNAME_BUFFER, PNAME_BUFFER structure pointer [NetBIOS], REGISTERED, REGISTERING, UNIQUE_NAME, nb30/NAME_BUFFER, nb30/PNAME_BUFFER, netbios.name_buffer'
f1_keywords:
- nb30/NAME_BUFFER
dev_langs:
- c++
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
- NAME_BUFFER
targetos: Windows
req.typenames: NAME_BUFFER, *PNAME_BUFFER
req.redist: 
ms.custom: 19H1
---

# NAME_BUFFER structure


## -description


<p class="CCE_Message">[<a href="https://docs.microsoft.com/previous-versions/windows/desktop/netbios/portal">Netbios</a> is not supported on Windows Vista,  Windows Server 2008, and subsequent versions of the operating system]

The <b>NAME_BUFFER</b> structure contains information about a local network name. One or more <b>NAME_BUFFER</b> structures follows an <a href="https://docs.microsoft.com/windows/desktop/api/nb30/ns-nb30-adapter_status">ADAPTER_STATUS</a> structure when an application specifies the <b>NCBASTAT</b> command in the ncb_command member of the <a href="https://docs.microsoft.com/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a> structure. 




## -struct-fields




### -field name

Specifies the local network name. This value is in the <b>ncb_name</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a> structure.


### -field name_num

Specifies the number for the local network name. This value is in the <b>ncb_num</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a> structure.


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








<a href="https://docs.microsoft.com/windows/desktop/api/nb30/ns-nb30-adapter_status">ADAPTER_STATUS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/nb30/ns-nb30-ncb">NCB</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/netbios/netbios-structures">NetBIOS Structures</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/netbios/portal">The NetBIOS Interface Overview</a>
 

 

