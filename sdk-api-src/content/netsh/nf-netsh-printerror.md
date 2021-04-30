---
UID: NF:netsh.PrintError
title: PrintError function (netsh.h)
description: Displays a system or application error message to the NetShell console.
helpviewer_keywords: ["PrintError","PrintError function [NetShell]","_netsh_printerror","netsh/PrintError","netshell.printerror"]
old-location: netshell\printerror.htm
tech.root: netshell
ms.assetid: de48b797-9cb5-4bc0-89d4-86dd7f56a610
ms.date: 12/05/2018
ms.keywords: PrintError, PrintError function [NetShell], _netsh_printerror, netsh/PrintError, netshell.printerror
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
req.lib: Netsh.lib
req.dll: Netsh.exe
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PrintError
 - netsh/PrintError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netsh.exe
api_name:
 - PrintError
---

# PrintError function


## -description

The 
<b>PrintError</b> function displays a system or application error message to the NetShell console.

## -parameters

### -param hModule [in]

A handle to the module from which the string should be loaded, or null for system error messages.

### -param dwErrId [in]

The identifier of the message to print.

### -param ...

The arguments used to fill into the message.

## -returns

Returns the number of characters printed. Returns zero upon failure.

## -see-also

<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-printmessage">PrintMessage</a>



<a href="/previous-versions/windows/desktop/api/netsh/nf-netsh-printmessagefrommodule">PrintMessageFromModule</a>

