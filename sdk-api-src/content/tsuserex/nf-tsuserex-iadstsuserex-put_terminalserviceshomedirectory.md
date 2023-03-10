---
UID: NF:tsuserex.IADsTSUserEx.put_TerminalServicesHomeDirectory
title: IADsTSUserEx::put_TerminalServicesHomeDirectory (tsuserex.h)
description: The root directory for the user. Each user on a Remote Desktop Session Host (RD Session Host) server has a unique root directory. This ensures that application information is stored separately for each user in a multiuser environment. (Put)
helpviewer_keywords: ["IADsTSUserEx interface [Remote Desktop Services]","TerminalServicesHomeDirectory property","IADsTSUserEx.TerminalServicesHomeDirectory","IADsTSUserEx.put_TerminalServicesHomeDirectory","IADsTSUserEx::TerminalServicesHomeDirectory","IADsTSUserEx::get_TerminalServicesHomeDirectory","IADsTSUserEx::put_TerminalServicesHomeDirectory","TerminalServicesHomeDirectory property [Remote Desktop Services]","TerminalServicesHomeDirectory property [Remote Desktop Services]","IADsTSUserEx interface","put_TerminalServicesHomeDirectory","termserv.iadstsuserex_terminalserviceshomedirectory","tsuserex/IADsTSUserEx::TerminalServicesHomeDirectory","tsuserex/IADsTSUserEx::get_TerminalServicesHomeDirectory","tsuserex/IADsTSUserEx::put_TerminalServicesHomeDirectory"]
old-location: termserv\iadstsuserex_terminalserviceshomedirectory.htm
tech.root: TermServ
ms.assetid: 3993b664-82bb-4419-a06f-2a4e24003170
ms.date: 12/05/2018
ms.keywords: IADsTSUserEx interface [Remote Desktop Services],TerminalServicesHomeDirectory property, IADsTSUserEx.TerminalServicesHomeDirectory, IADsTSUserEx.put_TerminalServicesHomeDirectory, IADsTSUserEx::TerminalServicesHomeDirectory, IADsTSUserEx::get_TerminalServicesHomeDirectory, IADsTSUserEx::put_TerminalServicesHomeDirectory, TerminalServicesHomeDirectory property [Remote Desktop Services], TerminalServicesHomeDirectory property [Remote Desktop Services],IADsTSUserEx interface, put_TerminalServicesHomeDirectory, termserv.iadstsuserex_terminalserviceshomedirectory, tsuserex/IADsTSUserEx::TerminalServicesHomeDirectory, tsuserex/IADsTSUserEx::get_TerminalServicesHomeDirectory, tsuserex/IADsTSUserEx::put_TerminalServicesHomeDirectory
req.header: tsuserex.h
req.include-header: Tsuserex.h, Tsuserex_i.c
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Tsuserex.tlb
req.lib: 
req.dll: Tsuserex.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsTSUserEx::put_TerminalServicesHomeDirectory
 - tsuserex/IADsTSUserEx::put_TerminalServicesHomeDirectory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tsuserex.dll
api_name:
 - IADsTSUserEx.TerminalServicesHomeDirectory
 - IADsTSUserEx.get_TerminalServicesHomeDirectory
 - IADsTSUserEx.put_TerminalServicesHomeDirectory
---

# IADsTSUserEx::put_TerminalServicesHomeDirectory


## -description

The root directory for the user. Each user on a Remote Desktop Session Host (RD Session Host) server has a unique root directory. This ensures that application information is stored separately for each user in a multiuser environment.

This property is read/write.

## -parameters

## -remarks

To set a root directory on the local computer, specify a local path; for example, C:\Path. To set a root directory in a network environment, you must first set the <a href="/windows/desktop/api/tsuserex/nf-tsuserex-iadstsuserex-get_terminalserviceshomedrive">TerminalServicesHomeDrive</a> property, and then set this property to a UNC path.


#### Examples

For an example, see <a href="/windows/desktop/api/tsuserex/nf-tsuserex-iadstsuserex-get_terminalserviceshomedrive">TerminalServicesHomeDrive</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/tsuserex/nn-tsuserex-iadstsuserex">IADsTSUserEx</a>
