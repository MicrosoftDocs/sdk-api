---
UID: NN:wuapi.IWindowsUpdateAgentInfo
title: IWindowsUpdateAgentInfo
author: windows-sdk-content
description: Retrieves information about the version of Windows Update Agent (WUA).
old-location: wua\iwindowsupdateagentinfo.htm
old-project: Wua_Sdk
ms.assetid: 46692b86-0fd9-4e48-9fb2-0ea3521b6bca
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWindowsUpdateAgentInfo, IWindowsUpdateAgentInfo interface [Windows Update Agent], IWindowsUpdateAgentInfo interface [Windows Update Agent],described, wua.iwindowsupdateagentinfo, wuapi/IWindowsUpdateAgentInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wuapi.h
req.include-header: 
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IWindowsUpdateAgentInfo
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IWindowsUpdateAgentInfo interface


## -description


Retrieves information about the version of Windows Update Agent (WUA).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowsUpdateAgentInfo</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWindowsUpdateAgentInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWindowsUpdateAgentInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451309">GetInfo</a>
</td>
<td align="left" width="63%">
Retrieves version information for WUA.

</td>
</tr>
</table> 


## -remarks



The <b>IWindowsUpdateAgentInfo</b> interface  may require  you to update WUA. For more information, see <a href="https://msdn.microsoft.com/829112ab-b240-4cc4-8053-18b484934886">Updating Windows Update Agent</a>.

You can create an instance of this interface by using the WindowsUpdateAgentInfo coclass. Use the Microsoft.Update.AgentInfo program identifier to create the object.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

