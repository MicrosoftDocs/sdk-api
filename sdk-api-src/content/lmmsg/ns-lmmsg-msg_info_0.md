---
UID: NS:lmmsg._MSG_INFO_0
title: MSG_INFO_0 (lmmsg.h)
description: The MSG_INFO_0 structure specifies a message alias.
helpviewer_keywords: ["*LPMSG_INFO_0","*PMSG_INFO_0","LPMSG_INFO_0","LPMSG_INFO_0 structure pointer [Network Management]","MSG_INFO_0","MSG_INFO_0 structure [Network Management]","PMSG_INFO_0","PMSG_INFO_0 structure pointer [Network Management]","_win32_msg_info_0_str","lmmsg/LPMSG_INFO_0","lmmsg/MSG_INFO_0","lmmsg/PMSG_INFO_0","netmgmt.msg_info_0_str"]
old-location: netmgmt\msg_info_0_str.htm
tech.root: NetMgmt
ms.assetid: bc409abd-8c76-4310-b9e3-05fc4e0d253e
ms.date: 12/05/2018
ms.keywords: '*LPMSG_INFO_0, *PMSG_INFO_0, LPMSG_INFO_0, LPMSG_INFO_0 structure pointer [Network Management], MSG_INFO_0, MSG_INFO_0 structure [Network Management], PMSG_INFO_0, PMSG_INFO_0 structure pointer [Network Management], _win32_msg_info_0_str, lmmsg/LPMSG_INFO_0, lmmsg/MSG_INFO_0, lmmsg/PMSG_INFO_0, netmgmt.msg_info_0_str'
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
targetos: Windows
req.typenames: MSG_INFO_0, *PMSG_INFO_0, *LPMSG_INFO_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MSG_INFO_0
 - lmmsg/_MSG_INFO_0
 - PMSG_INFO_0
 - lmmsg/PMSG_INFO_0
 - MSG_INFO_0
 - lmmsg/MSG_INFO_0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmmsg.h
api_name:
 - MSG_INFO_0
---

# MSG_INFO_0 structure


## -description

The
				<b>MSG_INFO_0</b> structure specifies a message alias.

## -struct-fields

### -field msgi0_name

Pointer to a Unicode string that specifies the alias to which the message is to be sent. The constant LEN specifies the maximum number of characters in the string.

## -see-also

<a href="/windows/desktop/NetMgmt/message-functions">Message Functions</a>



<a href="/windows/desktop/api/lmmsg/nf-lmmsg-netmessagenameenum">NetMessageNameEnum</a>



<a href="/windows/desktop/api/lmmsg/nf-lmmsg-netmessagenamegetinfo">NetMessageNameGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>