---
UID: NN:mmc.IConsolePower
title: IConsolePower (mmc.h)
author: windows-sdk-content
description: The IConsolePower interface controls the execution state and idle timers on operating systems that support power management.
old-location: mmc\iconsolepower.htm
tech.root: mmc
ms.assetid: d34e8da0-2689-4514-be10-4c11008432b3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ConsolePower, IConsolePower, IConsolePower interface [MMC], IConsolePower interface [MMC],described, _slate_iconsolepower, mmc.iconsolepower, mmc/IConsolePower
ms.topic: interface
req.header: mmc.h
req.include-header: 
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
req.type-library: 
req.lib: Mmc.lib
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsolePower
 - ConsolePower
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsolePower interface


## -description


The 
<b>IConsolePower</b> interface controls the execution state and idle timers on operating systems that support power management.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConsolePower</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IConsolePower</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConsolePower</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83de4b7f-3214-4354-a4a0-721054e2e899">ResetIdleTimer</a>
</td>
<td align="left" width="63%">
Resets idle timers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fbdc155-ea95-43b6-8aea-f47ff0c89859">SetExecutionState</a>
</td>
<td align="left" width="63%">
Sets the execution state.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/dd23c6dc-9219-4d13-b237-13405a2fcb5a">IConsolePowerSink</a>
 

 

