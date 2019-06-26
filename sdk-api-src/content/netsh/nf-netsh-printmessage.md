---
UID: NF:netsh.PrintMessage
title: PrintMessage function (netsh.h)
author: windows-sdk-content
description: Displays output to the NetShell console.
old-location: netshell\printmessage.htm
tech.root: netshell
ms.assetid: 6646a4f7-24b7-460c-8027-80485ac50785
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PrintMessage, PrintMessage function [NetShell], _netsh_printmessage, netsh/PrintMessage, netshell.printmessage
ms.topic: function
f1_keywords: 
 - "netsh/PrintMessage"
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
 - PrintMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PrintMessage function


## -description


The 
<b>PrintMessage</b> function displays output to the NetShell console.


## -parameters




### -param pwszFormat [in]

A string to be output to the NetShell console.


### -param arg2

The arguments used to fill into the message.


## -returns



Returns the number of characters printed. Returns zero upon failure.




## -remarks



Use the 
<b>PrintMessage</b> function when the message to be output is not required to be localized.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netsh/nf-netsh-printerror">PrintError</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netsh/nf-netsh-printmessagefrommodule">PrintMessageFromModule</a>
 

 

