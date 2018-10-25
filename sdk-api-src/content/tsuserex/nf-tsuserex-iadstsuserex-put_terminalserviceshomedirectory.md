---
UID: NF:tsuserex.IADsTSUserEx.put_TerminalServicesHomeDirectory
title: IADsTSUserEx::put_TerminalServicesHomeDirectory
author: windows-sdk-content
description: The root directory for the user. Each user on a Remote Desktop Session Host (RD Session Host) server has a unique root directory. This ensures that application information is stored separately for each user in a multiuser environment.
old-location: termserv\iadstsuserex_terminalserviceshomedirectory.htm
tech.root: termserv
ms.assetid: 3993b664-82bb-4419-a06f-2a4e24003170
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: IADsTSUserEx interface [Remote Desktop Services],TerminalServicesHomeDirectory property, IADsTSUserEx.TerminalServicesHomeDirectory, IADsTSUserEx.put_TerminalServicesHomeDirectory, IADsTSUserEx::TerminalServicesHomeDirectory, IADsTSUserEx::get_TerminalServicesHomeDirectory, IADsTSUserEx::put_TerminalServicesHomeDirectory, TerminalServicesHomeDirectory property [Remote Desktop Services], TerminalServicesHomeDirectory property [Remote Desktop Services],IADsTSUserEx interface, put_TerminalServicesHomeDirectory, termserv.iadstsuserex_terminalserviceshomedirectory, tsuserex/IADsTSUserEx::TerminalServicesHomeDirectory, tsuserex/IADsTSUserEx::get_TerminalServicesHomeDirectory, tsuserex/IADsTSUserEx::put_TerminalServicesHomeDirectory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IADsTSUserEx.TerminalServicesHomeDirectory
 - IADsTSUserEx.get_TerminalServicesHomeDirectory
 - IADsTSUserEx.put_TerminalServicesHomeDirectory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsTSUserEx::put_TerminalServicesHomeDirectory


## -description


The root directory for the user. Each user on a Remote Desktop Session Host (RD Session Host) server has a unique root directory. This ensures that application information is stored separately for each user in a multiuser environment.

This property is read/write.


## -parameters


## -remarks



To set a root directory on the local computer, specify a local path; for example, C:\Path. To set a root directory in a network environment, you must first set the <a href="https://msdn.microsoft.com/e5cfa526-eff8-4a89-9b13-c4a06a416fe5">TerminalServicesHomeDrive</a> property, and then set this property to a UNC path.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/e5cfa526-eff8-4a89-9b13-c4a06a416fe5">TerminalServicesHomeDrive</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7af8fe94-15db-49dc-ba4a-b79601205f59">IADsTSUserEx</a>
 

 

