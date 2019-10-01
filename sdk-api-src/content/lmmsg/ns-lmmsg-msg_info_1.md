---
UID: NS:lmmsg._MSG_INFO_1
title: MSG_INFO_1 (lmmsg.h)
author: windows-sdk-content
description: The MSG_INFO_1 structure specifies a message alias. This structure exists only for compatibility. Message forwarding is not supported.
old-location: netmgmt\msg_info_1_str.htm
tech.root: NetMgmt
ms.assetid: 6abb2622-6fa4-460a-b300-feaf548ba648
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPMSG_INFO_1, *PMSG_INFO_1, LPMSG_INFO_1, LPMSG_INFO_1 structure pointer [Network Management], MSG_INFO_1, MSG_INFO_1 structure [Network Management], PMSG_INFO_1, PMSG_INFO_1 structure pointer [Network Management], _win32_msg_info_1_str, lmmsg/LPMSG_INFO_1, lmmsg/MSG_INFO_1, lmmsg/PMSG_INFO_1, netmgmt.msg_info_1_str"
ms.topic: struct
f1_keywords: 
 - "lmmsg/MSG_INFO_1"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmmsg.h
api_name:
 - MSG_INFO_1
targetos: Windows
req.typenames: MSG_INFO_1, *PMSG_INFO_1, *LPMSG_INFO_1
req.redist: 
ms.custom: 19H1
---

# MSG_INFO_1 structure


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




<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/message-functions">Message Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmmsg/nf-lmmsg-netmessagenameenum">NetMessageNameEnum</a>



<a href="https://docs.microsoft.com/windows/desktop/api/lmmsg/nf-lmmsg-netmessagenamegetinfo">NetMessageNameGetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>
 

 

