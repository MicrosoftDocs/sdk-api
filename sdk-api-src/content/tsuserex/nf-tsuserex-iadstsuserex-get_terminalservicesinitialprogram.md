---
UID: NF:tsuserex.IADsTSUserEx.get_TerminalServicesInitialProgram
title: IADsTSUserEx::get_TerminalServicesInitialProgram (tsuserex.h)
description: The path and file name of the application that the user wants to start automatically when the user logs on to the Remote Desktop Session Host (RD Session Host) server. (Get)
helpviewer_keywords: ["IADsTSUserEx interface [Remote Desktop Services]","TerminalServicesInitialProgram property","IADsTSUserEx.TerminalServicesInitialProgram","IADsTSUserEx.get_TerminalServicesInitialProgram","IADsTSUserEx::TerminalServicesInitialProgram","IADsTSUserEx::get_TerminalServicesInitialProgram","IADsTSUserEx::put_TerminalServicesInitialProgram","TerminalServicesInitialProgram property [Remote Desktop Services]","TerminalServicesInitialProgram property [Remote Desktop Services]","IADsTSUserEx interface","get_TerminalServicesInitialProgram","termserv.iadstsuserex_terminalservicesinitialprogram","tsuserex/IADsTSUserEx::TerminalServicesInitialProgram","tsuserex/IADsTSUserEx::get_TerminalServicesInitialProgram","tsuserex/IADsTSUserEx::put_TerminalServicesInitialProgram"]
old-location: termserv\iadstsuserex_terminalservicesinitialprogram.htm
tech.root: TermServ
ms.assetid: 43059f13-a1f1-44b2-96ac-2532656a0846
ms.date: 12/05/2018
ms.keywords: IADsTSUserEx interface [Remote Desktop Services],TerminalServicesInitialProgram property, IADsTSUserEx.TerminalServicesInitialProgram, IADsTSUserEx.get_TerminalServicesInitialProgram, IADsTSUserEx::TerminalServicesInitialProgram, IADsTSUserEx::get_TerminalServicesInitialProgram, IADsTSUserEx::put_TerminalServicesInitialProgram, TerminalServicesInitialProgram property [Remote Desktop Services], TerminalServicesInitialProgram property [Remote Desktop Services],IADsTSUserEx interface, get_TerminalServicesInitialProgram, termserv.iadstsuserex_terminalservicesinitialprogram, tsuserex/IADsTSUserEx::TerminalServicesInitialProgram, tsuserex/IADsTSUserEx::get_TerminalServicesInitialProgram, tsuserex/IADsTSUserEx::put_TerminalServicesInitialProgram
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
 - IADsTSUserEx::get_TerminalServicesInitialProgram
 - tsuserex/IADsTSUserEx::get_TerminalServicesInitialProgram
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
 - IADsTSUserEx.TerminalServicesInitialProgram
 - IADsTSUserEx.get_TerminalServicesInitialProgram
 - IADsTSUserEx.put_TerminalServicesInitialProgram
---

# IADsTSUserEx::get_TerminalServicesInitialProgram


## -description

The path and file name of the application that the user wants to start automatically when the user logs on to the Remote Desktop Session Host (RD Session Host) server.

This property is read/write.

## -parameters

## -remarks

To set an initial application to start when the user logs on, you must first set this property and then set the <a href="/windows/desktop/api/tsuserex/nf-tsuserex-iadstsuserex-get_terminalservicesworkdirectory">TerminalServicesWorkDirectory</a> property. If you set only the <b>TerminalServicesInitialProgram</b> property, the application starts in the user's session in the default user directory.


#### Examples

The following example shows a script that binds to the Active Directory database without credentials.


```vb
Set DSO = GetObject("LDAP:")
Set usr = DSO.OpenDSObject(
    "LDAP://DOMAIN/CN=Test,CN=Users,DC=Server1,DC=Domain,DC=com")
Wscript.echo usr.TerminalServicesWorkDirectory
Wscript.echo usr.TerminalServicesInitialProgram
usr.TerminalServicesInitialProgram= "cmd.exe"
usr.TerminalServicesWorkDirectory= "D:\path"
usr.SetInfo
WScript.echo usr.TerminalServicesInitialProgram
Wscript.echo usr.TerminalServicesWorkDirectory

```

## -see-also

<a href="/windows/desktop/api/tsuserex/nn-tsuserex-iadstsuserex">IADsTSUserEx</a>
