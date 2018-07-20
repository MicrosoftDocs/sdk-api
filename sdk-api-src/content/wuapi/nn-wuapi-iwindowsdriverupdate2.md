---
UID: NN:wuapi.IWindowsDriverUpdate2
title: IWindowsDriverUpdate2
author: windows-sdk-content
description: Contains the properties and methods that are available only from a Windows driver update.
old-location: wua\iwindowsdriverupdate2.htm
old-project: Wua_Sdk
ms.assetid: 9a2d6318-c5f0-41bc-a4df-bb9a53c9dee4
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IWindowsDriverUpdate2, IWindowsDriverUpdate2 interface [Windows Update Agent], IWindowsDriverUpdate2 interface [Windows Update Agent],described, wua.iwindowsdriverupdate2, wuapi/IWindowsDriverUpdate2
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IWindowsDriverUpdate2
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IWindowsDriverUpdate2 interface


## -description


Contains the properties and methods that are available only from a Windows driver update.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowsDriverUpdate2</b> interface inherits from <a href="https://msdn.microsoft.com/4e2eda04-4f86-4919-b754-dba90fa8d5d8">IWindowsDriverUpdate</a>. <b>IWindowsDriverUpdate2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IWindowsDriverUpdate2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ad3f1bf-8da3-4d7d-8ed9-508422782861">CopyToCache</a>
</td>
<td align="left" width="63%">
Copies the external update binaries to an update.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowsDriverUpdate2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6399d545-b300-4f78-b6df-c9892bc62fbb">CveIDs</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a collection of the Common Vulnerabilities and Exposures (CVE) identifiers that are associated with an update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn949436">IsPresent</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether an update is installed on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/32c6982e-9654-4f8f-acca-ba1e4d52b210">RebootRequired</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the computer must be restarted after you install or uninstall an update.

</td>
</tr>
</table> 


## -remarks



This interface can be obtained by calling <a href="https://msdn.microsoft.com/library/ms682521(v=VS.85).aspx">QueryInterface</a> method on an <a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a> interface only if the interface represents a Windows Driver update.




## -see-also




<a href="https://msdn.microsoft.com/4e2eda04-4f86-4919-b754-dba90fa8d5d8">IWindowsDriverUpdate</a>
 

 

