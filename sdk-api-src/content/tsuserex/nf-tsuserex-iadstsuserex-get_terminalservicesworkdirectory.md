---
UID: NF:tsuserex.IADsTSUserEx.get_TerminalServicesWorkDirectory
title: IADsTSUserEx::get_TerminalServicesWorkDirectory
author: windows-sdk-content
description: The working directory path for the user.
old-location: termserv\iadstsuserex_terminalservicesworkdirectory.htm
tech.root: termserv
ms.assetid: 66048329-ae5a-4e70-b6a4-dcdc312a74df
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IADsTSUserEx interface [Remote Desktop Services],TerminalServicesWorkDirectory property, IADsTSUserEx.TerminalServicesWorkDirectory, IADsTSUserEx.get_TerminalServicesWorkDirectory, IADsTSUserEx::TerminalServicesWorkDirectory, IADsTSUserEx::get_TerminalServicesWorkDirectory, IADsTSUserEx::put_TerminalServicesWorkDirectory, TerminalServicesWorkDirectory property [Remote Desktop Services], TerminalServicesWorkDirectory property [Remote Desktop Services],IADsTSUserEx interface, get_TerminalServicesWorkDirectory, termserv.iadstsuserex_terminalservicesworkdirectory, tsuserex/IADsTSUserEx::TerminalServicesWorkDirectory, tsuserex/IADsTSUserEx::get_TerminalServicesWorkDirectory, tsuserex/IADsTSUserEx::put_TerminalServicesWorkDirectory
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
 - IADsTSUserEx.TerminalServicesWorkDirectory
 - IADsTSUserEx.get_TerminalServicesWorkDirectory
 - IADsTSUserEx.put_TerminalServicesWorkDirectory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tsuserex.h
: 
- IADsTSUserEx.get_TerminalServicesWorkDirectory
: 
---

# IADsTSUserEx::get_TerminalServicesWorkDirectory


## -description


The working directory path for the user.

This property is read/write.


## -parameters


## -remarks



To set an initial application to start when the user logs on to the Remote Desktop Session Host (RD Session Host) server, you must first set the <a href="https://msdn.microsoft.com/43059f13-a1f1-44b2-96ac-2532656a0846">TerminalServicesInitialProgram</a> property, and then set this property.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/43059f13-a1f1-44b2-96ac-2532656a0846">TerminalServicesInitialProgram</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7af8fe94-15db-49dc-ba4a-b79601205f59">IADsTSUserEx</a>
 

 

