---
UID: NF:tsuserex.IADsTSUserEx.get_TerminalServicesWorkDirectory
title: IADsTSUserEx::get_TerminalServicesWorkDirectory (tsuserex.h)
description: The working directory path for the user.helpviewer_keywords: ["IADsTSUserEx interface [Remote Desktop Services]","TerminalServicesWorkDirectory property","IADsTSUserEx.TerminalServicesWorkDirectory","IADsTSUserEx.get_TerminalServicesWorkDirectory","IADsTSUserEx::TerminalServicesWorkDirectory","IADsTSUserEx::get_TerminalServicesWorkDirectory","IADsTSUserEx::put_TerminalServicesWorkDirectory","TerminalServicesWorkDirectory property [Remote Desktop Services]","TerminalServicesWorkDirectory property [Remote Desktop Services]","IADsTSUserEx interface","get_TerminalServicesWorkDirectory","termserv.iadstsuserex_terminalservicesworkdirectory","tsuserex/IADsTSUserEx::TerminalServicesWorkDirectory","tsuserex/IADsTSUserEx::get_TerminalServicesWorkDirectory","tsuserex/IADsTSUserEx::put_TerminalServicesWorkDirectory"]
old-location: termserv\iadstsuserex_terminalservicesworkdirectory.htm
tech.root: TermServ
ms.assetid: 66048329-ae5a-4e70-b6a4-dcdc312a74df
ms.date: 12/05/2018
ms.keywords: IADsTSUserEx interface [Remote Desktop Services],TerminalServicesWorkDirectory property, IADsTSUserEx.TerminalServicesWorkDirectory, IADsTSUserEx.get_TerminalServicesWorkDirectory, IADsTSUserEx::TerminalServicesWorkDirectory, IADsTSUserEx::get_TerminalServicesWorkDirectory, IADsTSUserEx::put_TerminalServicesWorkDirectory, TerminalServicesWorkDirectory property [Remote Desktop Services], TerminalServicesWorkDirectory property [Remote Desktop Services],IADsTSUserEx interface, get_TerminalServicesWorkDirectory, termserv.iadstsuserex_terminalservicesworkdirectory, tsuserex/IADsTSUserEx::TerminalServicesWorkDirectory, tsuserex/IADsTSUserEx::get_TerminalServicesWorkDirectory, tsuserex/IADsTSUserEx::put_TerminalServicesWorkDirectory
f1_keywords:
- tsuserex/IADsTSUserEx.TerminalServicesWorkDirectory
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tsuserex.dll
api_name:
- IADsTSUserEx.TerminalServicesWorkDirectory
- IADsTSUserEx.get_TerminalServicesWorkDirectory
- IADsTSUserEx.put_TerminalServicesWorkDirectory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsTSUserEx::get_TerminalServicesWorkDirectory


## -description


The working directory path for the user.

This property is read/write.


## -parameters


## -remarks



To set an initial application to start when the user logs on to the Remote Desktop Session Host (RD Session Host) server, you must first set the <a href="https://docs.microsoft.com/windows/desktop/api/tsuserex/nf-tsuserex-iadstsuserex-get_terminalservicesinitialprogram">TerminalServicesInitialProgram</a> property, and then set this property.


#### Examples

For an example, see <a href="https://docs.microsoft.com/windows/desktop/api/tsuserex/nf-tsuserex-iadstsuserex-get_terminalservicesinitialprogram">TerminalServicesInitialProgram</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tsuserex/nn-tsuserex-iadstsuserex">IADsTSUserEx</a>
 

 

