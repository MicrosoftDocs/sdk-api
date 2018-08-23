---
UID: NN:wuapi.IInstallationAgent
title: IInstallationAgent
author: windows-sdk-content
description: Records the result for an update.
old-location: wua\iinstallationagent.htm
old-project: wua_sdk
ms.assetid: B24B527C-D92B-4BEB-ADCC-5E2BA684A478
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IInstallationAgent, IInstallationAgent interface [Windows Update Agent], IInstallationAgent interface [Windows Update Agent],described, wua.iinstallationagent, wuapi/IInstallationAgent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wuapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IInstallationAgent
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IInstallationAgent interface


## -description


Records the result for an update.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInstallationAgent</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IInstallationAgent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInstallationAgent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E2DD54E3-741E-4647-9993-A9476279BD6C">RecordInstallationResult</a>
</td>
<td align="left" width="63%">
Records the result for an update. The result is specified by an <a href="https://msdn.microsoft.com/3aaab669-1f80-41ee-8c29-6da613ebccff">IStringCollection</a> object.

</td>
</tr>
</table> 

