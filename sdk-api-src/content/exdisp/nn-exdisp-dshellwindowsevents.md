---
UID: NN:exdisp.DShellWindowsEvents
title: DShellWindowsEvents
author: windows-driver-content
description: Receives IShellWindows window registration events.
old-location: shell\DShellWindowsEvents.htm
old-project: shell
ms.assetid: c340296d-f8eb-43a1-809d-912ea7412fe2
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: DShellWindowsEvents, DShellWindowsEvents object [Windows Shell], DShellWindowsEvents object [Windows Shell], described, _win32_DShellWindowsEvents, exdisp/DShellWindowsEvents, shell.DShellWindowsEvents
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: exdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ShellWindowTypeConstants
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shdocvw.dll
api_name:
-	DShellWindowsEvents
product: Windows
targetos: Windows
req.lib: Shdocvw.dll
req.dll: Shdocvw.dll (version 5.00.2014.0216 or later)
req.irql: 
req.product: Internet Explorer 5
---

# DShellWindowsEvents interface


## -description



        Receives <a href="https://msdn.microsoft.com/e609c8b6-2b2e-4188-894c-5c85960206ea">IShellWindows</a> window registration events.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">DShellWindowsEvents</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>DShellWindowsEvents</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7faf758a-daa0-47f5-9f95-61fe3d8286ea">WindowRegistered</a>
</td>
<td align="left" width="63%">

        Called when a window is registered as a Shell window.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92e8653f-7f41-4e0b-97e5-429fddc51951">WindowRevoked</a>
</td>
<td align="left" width="63%">

        Called when a Shell window's registration is revoked.
        

</td>
</tr>
</table> 


## -remarks




            Use <b>DShellWindowsEvents</b> to monitor when a Shell window is registered or revoked.  For more information, see <a href="https://msdn.microsoft.com/e609c8b6-2b2e-4188-894c-5c85960206ea">IShellWindows</a>.
            




## -see-also




<a href="https://msdn.microsoft.com/cad1f961-7fb4-4ba1-be48-b664d3de2c60">ShellWindows</a>
 

 

