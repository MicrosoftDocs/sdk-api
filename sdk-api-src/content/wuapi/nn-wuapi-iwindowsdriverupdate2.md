---
UID: NN:wuapi.IWindowsDriverUpdate2
title: IWindowsDriverUpdate2 (wuapi.h)
author: windows-sdk-content
description: Contains the properties and methods that are available only from a Windows driver update.
old-location: wua\iwindowsdriverupdate2.htm
tech.root: Wua_Sdk
ms.assetid: 9a2d6318-c5f0-41bc-a4df-bb9a53c9dee4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWindowsDriverUpdate2, IWindowsDriverUpdate2 interface [Windows Update Agent], IWindowsDriverUpdate2 interface [Windows Update Agent],described, wua.iwindowsdriverupdate2, wuapi/IWindowsDriverUpdate2
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
 - IWindowsDriverUpdate2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWindowsDriverUpdate2 interface


## -description


Contains the properties and methods that are available only from a Windows driver update.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowsDriverUpdate2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iwindowsdriverupdate">IWindowsDriverUpdate</a>. <b>IWindowsDriverUpdate2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iwindowsdriverupdate2-copytocache">CopyToCache</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iwindowsdriverupdate2-get_cveids">CveIDs</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iwindowsdriverupdate2-get_ispresent">IsPresent</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iwindowsdriverupdate2-get_rebootrequired">RebootRequired</a>


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



This interface can be obtained by calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method on an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a> interface only if the interface represents a Windows Driver update.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iwindowsdriverupdate">IWindowsDriverUpdate</a>
 

 

