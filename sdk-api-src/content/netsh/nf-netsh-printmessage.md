---
UID: NF:netsh.PrintMessage
title: PrintMessage function
author: windows-sdk-content
description: Displays output to the NetShell console.
old-location: netshell\printmessage.htm
old-project: NetShell
ms.assetid: 6646a4f7-24b7-460c-8027-80485ac50785
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PrintMessage, PrintMessage function [NetShell], _netsh_printmessage, netsh/PrintMessage, netshell.printmessage
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: NS_REQS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Netsh.exe
api_name:
-	PrintMessage
product: Windows
targetos: Windows
req.lib: Netsh.lib
req.dll: Netsh.exe
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PrintMessage function


## -description


The 
<b>PrintMessage</b> function displays output to the NetShell console.


## -parameters




### -param pwszFormat

TBD


### -param param

TBD




####### - ...


					The arguments used to fill into the message.


#### - rgwcInput [in]

A string to be output to the NetShell console.


## -returns



Returns the number of characters printed. Returns zero upon failure.




## -remarks



Use the 
<b>PrintMessage</b> function when the message to be output is not required to be localized.




## -see-also




<a href="https://msdn.microsoft.com/de48b797-9cb5-4bc0-89d4-86dd7f56a610">PrintError</a>



<a href="https://msdn.microsoft.com/21f4688a-24fd-40b3-8da4-08c496b395f3">PrintMessageFromModule</a>
 

 

