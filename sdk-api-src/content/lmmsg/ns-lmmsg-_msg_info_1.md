---
UID: NS:lmmsg._MSG_INFO_1
title: "_MSG_INFO_1"
author: windows-sdk-content
description: The MSG_INFO_1 structure specifies a message alias. This structure exists only for compatibility. Message forwarding is not supported.
old-location: netmgmt\msg_info_1_str.htm
old-project: netmgmt
ms.assetid: 6abb2622-6fa4-460a-b300-feaf548ba648
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPMSG_INFO_1, *PMSG_INFO_1, LPMSG_INFO_1, LPMSG_INFO_1 structure pointer [Network Management], MSG_INFO_1, MSG_INFO_1 structure [Network Management], PMSG_INFO_1, PMSG_INFO_1 structure pointer [Network Management], _MSG_INFO_1, _win32_msg_info_1_str, lmmsg/LPMSG_INFO_1, lmmsg/MSG_INFO_1, lmmsg/PMSG_INFO_1, netmgmt.msg_info_1_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lmmsg.h
req.include-header: Lm.h
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
req.typenames: MSG_INFO_1, *PMSG_INFO_1, *LPMSG_INFO_1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmmsg.h
api_name:
 - MSG_INFO_1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MSG_INFO_1 structure


## -description


The
				<b>MSG_INFO_1</b> structure specifies a message alias. This structure exists only for compatibility. Message forwarding is not supported.


## -struct-fields




### -field msgi1_name

Pointer to a Unicode string that specifies the alias to which the message is to be sent. The constant LEN specifies the maximum number of characters in the string.


### -field msgi1_forward_flag

This member must be zero.


### -field msgi1_forward

This member must be <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/9face737-3472-4a53-97b6-e861a60ee96a">Message Functions</a>



<a href="https://msdn.microsoft.com/fc1b11e6-294d-47d3-8c63-bee80b5a8581">NetMessageNameEnum</a>



<a href="https://msdn.microsoft.com/72129865-2aee-41d5-8a89-53bb815a7f63">NetMessageNameGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

