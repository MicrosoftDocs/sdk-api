---
UID: NN:wuapi.IUpdateSession3
title: IUpdateSession3 (wuapi.h)
author: windows-sdk-content
description: Represents a session in which the caller can perform operations that involve updates. For example, this interface represents sessions in which the caller performs a search, download, installation, or uninstallation operation.
old-location: wua\iupdatesession3.htm
tech.root: Wua_Sdk
ms.assetid: 7caa07ee-ec78-45eb-99a2-0e6682790c88
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUpdateSession3, IUpdateSession3 interface [Windows Update Agent], IUpdateSession3 interface [Windows Update Agent],described, wua.iupdatesession3, wuapi/IUpdateSession3
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
 - IUpdateSession3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUpdateSession3 interface


## -description


Represents a session in which the caller can perform operations that involve updates. For example, this interface represents sessions in which the caller performs a search, download, installation, or uninstallation operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUpdateSession3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatesession2">IUpdateSession2</a>. <b>IUpdateSession3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUpdateSession3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesession3-createupdateservicemanager">CreateUpdateServiceManager</a>
</td>
<td align="left" width="63%">
Returns a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdateservicemanager2">IUpdateServiceManager2</a> interface for the session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesession3-queryhistory">QueryHistory</a>
</td>
<td align="left" width="63%">
Returns a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatehistoryentrycollection">IUpdateHistoryEntryCollection</a> interface. The interface contains matching event records on the computer. This causes the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesession3-queryhistory">QueryHistory</a> method to synchronously query the computer for the history of update events.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatesession2">IUpdateSession2</a>
 

 

