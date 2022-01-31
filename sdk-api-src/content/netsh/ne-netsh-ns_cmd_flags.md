---
UID: NE:netsh.NS_CMD_FLAGS
title: NS_CMD_FLAGS (netsh.h)
description: Specifies command flags available in NetShell.
helpviewer_keywords: ["CMD_FLAG_HIDDEN","CMD_FLAG_INTERACTIVE","CMD_FLAG_LIMIT_MASK","CMD_FLAG_LOCAL","CMD_FLAG_ONLINE","CMD_FLAG_PRIORITY","CMD_FLAG_PRIVATE","NS_CMD_FLAGS","NS_CMD_FLAGS enumeration [NetShell]","netsh/CMD_FLAG_HIDDEN","netsh/CMD_FLAG_INTERACTIVE","netsh/CMD_FLAG_LIMIT_MASK","netsh/CMD_FLAG_LOCAL","netsh/CMD_FLAG_ONLINE","netsh/CMD_FLAG_PRIORITY","netsh/CMD_FLAG_PRIVATE","netsh/NS_CMD_FLAGS","netshell.ns_cmd_flags"]
old-location: netshell\ns_cmd_flags.htm
tech.root: netshell
ms.assetid: ecf4580a-c03c-4589-9cf8-f6498a3d33d9
ms.date: 12/05/2018
ms.keywords: CMD_FLAG_HIDDEN, CMD_FLAG_INTERACTIVE, CMD_FLAG_LIMIT_MASK, CMD_FLAG_LOCAL, CMD_FLAG_ONLINE, CMD_FLAG_PRIORITY, CMD_FLAG_PRIVATE, NS_CMD_FLAGS, NS_CMD_FLAGS enumeration [NetShell], netsh/CMD_FLAG_HIDDEN, netsh/CMD_FLAG_INTERACTIVE, netsh/CMD_FLAG_LIMIT_MASK, netsh/CMD_FLAG_LOCAL, netsh/CMD_FLAG_ONLINE, netsh/CMD_FLAG_PRIORITY, netsh/CMD_FLAG_PRIVATE, netsh/NS_CMD_FLAGS, netshell.ns_cmd_flags
req.header: netsh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NS_CMD_FLAGS
 - netsh/NS_CMD_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netsh.h
api_name:
 - NS_CMD_FLAGS
---

# NS_CMD_FLAGS enumeration


## -description

The <b>NS_CMD_FLAGS</b> enumeration specifies command flags available in NetShell.

## -enum-fields

### -field CMD_FLAG_PRIVATE:0x01

Indicates a private command. This command is not valid in subcontexts.

### -field CMD_FLAG_INTERACTIVE:0x02

Indicates an interactive command. This command is not valid from outside NetShell.

### -field CMD_FLAG_LOCAL:0x08

Indicates a local command. This command is not valid from remote computers.

### -field CMD_FLAG_ONLINE:0x10

Indicates a command is valid only when online. This command is not valid in offline or noncommit mode.

### -field CMD_FLAG_HIDDEN:0x20

Indicates a command is not in online Help, but can be executed.

### -field CMD_FLAG_LIMIT_MASK:0xffff

Indicates that the  command limits the mask.

### -field CMD_FLAG_PRIORITY

Indicates that the <b>ulPriority</b> field is used.

