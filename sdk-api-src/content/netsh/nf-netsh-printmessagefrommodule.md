---
UID: NF:netsh.PrintMessageFromModule
title: PrintMessageFromModule function (netsh.h)
author: windows-sdk-content
description: Displays localized output to the NetShell console.
old-location: netshell\printmessagefrommodule.htm
tech.root: netshell
ms.assetid: 21f4688a-24fd-40b3-8da4-08c496b395f3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PrintMessageFromModule, PrintMessageFromModule function [NetShell], _netsh_printmessagefrommodule, netsh/PrintMessageFromModule, netshell.printmessagefrommodule
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netsh.exe
api_name:
 - PrintMessageFromModule
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PrintMessageFromModule function


## -description


The 
<b>PrintMessageFromModule</b> function displays localized output to the NetShell console.


## -parameters




### -param hModule [in]

A handle to the module from which the string should be loaded.


### -param dwMsgId [in]

The identifier  of the message to print.


### -param arg3

The arguments to fill into the message.


## -returns



Returns the number of characters printed. Returns zero upon failure.




## -remarks



Use this function when the format string, identified by the <i>dwMsgId</i> parameter, must be localized.




## -see-also




<a href="https://msdn.microsoft.com/de48b797-9cb5-4bc0-89d4-86dd7f56a610">PrintError</a>



<a href="https://msdn.microsoft.com/6646a4f7-24b7-460c-8027-80485ac50785">PrintMessage</a>
 

 

