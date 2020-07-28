---
UID: NF:tsuserex.IADsTSUserEx.get_TerminalServicesHomeDrive
title: IADsTSUserEx::get_TerminalServicesHomeDrive (tsuserex.h)
description: The root drive for the user. In a network environment, this property is a string that contains a drive specification (a drive letter followed by a colon) to which the UNC path specified as the root directory is mapped.
helpviewer_keywords: ["IADsTSUserEx interface [Remote Desktop Services]","TerminalServicesHomeDrive property","IADsTSUserEx.TerminalServicesHomeDrive","IADsTSUserEx.get_TerminalServicesHomeDrive","IADsTSUserEx::TerminalServicesHomeDrive","IADsTSUserEx::get_TerminalServicesHomeDrive","IADsTSUserEx::put_TerminalServicesHomeDrive","TerminalServicesHomeDrive property [Remote Desktop Services]","TerminalServicesHomeDrive property [Remote Desktop Services]","IADsTSUserEx interface","get_TerminalServicesHomeDrive","termserv.iadstsuserex_terminalserviceshomedrive","tsuserex/IADsTSUserEx::TerminalServicesHomeDrive","tsuserex/IADsTSUserEx::get_TerminalServicesHomeDrive","tsuserex/IADsTSUserEx::put_TerminalServicesHomeDrive"]
old-location: termserv\iadstsuserex_terminalserviceshomedrive.htm
tech.root: TermServ
ms.assetid: e5cfa526-eff8-4a89-9b13-c4a06a416fe5
ms.date: 12/05/2018
ms.keywords: IADsTSUserEx interface [Remote Desktop Services],TerminalServicesHomeDrive property, IADsTSUserEx.TerminalServicesHomeDrive, IADsTSUserEx.get_TerminalServicesHomeDrive, IADsTSUserEx::TerminalServicesHomeDrive, IADsTSUserEx::get_TerminalServicesHomeDrive, IADsTSUserEx::put_TerminalServicesHomeDrive, TerminalServicesHomeDrive property [Remote Desktop Services], TerminalServicesHomeDrive property [Remote Desktop Services],IADsTSUserEx interface, get_TerminalServicesHomeDrive, termserv.iadstsuserex_terminalserviceshomedrive, tsuserex/IADsTSUserEx::TerminalServicesHomeDrive, tsuserex/IADsTSUserEx::get_TerminalServicesHomeDrive, tsuserex/IADsTSUserEx::put_TerminalServicesHomeDrive
f1_keywords:
- tsuserex/IADsTSUserEx.TerminalServicesHomeDrive
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
- IADsTSUserEx.TerminalServicesHomeDrive
- IADsTSUserEx.get_TerminalServicesHomeDrive
- IADsTSUserEx.put_TerminalServicesHomeDrive
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsTSUserEx::get_TerminalServicesHomeDrive


## -description


The root drive for the user. In a network environment, this property is a string that contains a drive specification (a drive letter followed by a colon) to which the UNC path specified as the root directory is mapped.

This property is read/write.


## -parameters


## -remarks



To set a root directory in a network environment, you must first set this property and then set the <a href="https://docs.microsoft.com/windows/desktop/api/tsuserex/nf-tsuserex-iadstsuserex-get_terminalserviceshomedirectory">TerminalServicesHomeDirectory</a> property.


#### Examples

The following example shows a script that binds to the SAM database without credentials.


```vb
Set DSO = GetObject("WinNT:")
Set usr = DSO.OpenDSObject("WinNT://Server1/Test,user")
WScript.echo usr.TerminalServicesHomeDrive
Wscript.echo usr.TerminalServicesHomeDirectory

usr.TerminalServicesHomeDrive = "Z:"
usr.TerminalServicesHomeDirectory = "\\servername\share\path"
usr.SetInfo

WScript.echo usr.TerminalServicesHomeDrive
WScript.echo usr.TerminalServicesHomeDirectory

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tsuserex/nn-tsuserex-iadstsuserex">IADsTSUserEx</a>
 

 

