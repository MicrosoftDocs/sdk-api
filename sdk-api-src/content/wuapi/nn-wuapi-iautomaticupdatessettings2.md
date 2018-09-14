---
UID: NN:wuapi.IAutomaticUpdatesSettings2
title: IAutomaticUpdatesSettings2
author: windows-sdk-content
description: Contains the settings that are available in Automatic Updates.
old-location: wua\iautomaticupdatessettings2.htm
tech.root: Wua_Sdk
ms.assetid: 5ad1a3ee-3293-4825-a85e-ca1e3a38e775
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IAutomaticUpdatesSettings2, IAutomaticUpdatesSettings2 interface [Windows Update Agent], IAutomaticUpdatesSettings2 interface [Windows Update Agent],described, wua.iautomaticupdatessettings2, wuapi/IAutomaticUpdatesSettings2
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
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IAutomaticUpdatesSettings2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAutomaticUpdatesSettings2 interface


## -description


Contains the settings that are available in Automatic Updates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAutomaticUpdatesSettings2</b> interface inherits from <a href="https://msdn.microsoft.com/c4672df5-9e47-45f5-9504-1ebb0bf3c6a6">IAutomaticUpdatesSettings</a>. <b>IAutomaticUpdatesSettings2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IAutomaticUpdatesSettings2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbf36d9f-98c1-4b9d-b479-a9203b6ce952">CheckPermission</a>
</td>
<td align="left" width="63%">
Determines whether a specific user or type of user has permission to perform a selected action.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAutomaticUpdatesSettings2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/502b0490-8834-496a-8691-d9325ad86799">IncludeRecommendedUpdates</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a Boolean value that indicates whether to include optional or recommended updates when a  search for updates and installation of updates is performed.

</td>
</tr>
</table> 


## -remarks



The <b>IAutomaticUpdatesSettings2</b> interface  may require you to update the Windows Update Agent (WUA). For more information, see <a href="https://msdn.microsoft.com/829112ab-b240-4cc4-8053-18b484934886">Updating Windows Update Agent</a>.




## -see-also




<a href="https://msdn.microsoft.com/c4672df5-9e47-45f5-9504-1ebb0bf3c6a6">IAutomaticUpdatesSettings</a>
 

 

