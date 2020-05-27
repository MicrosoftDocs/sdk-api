---
UID: NN:wuapi.IInstallationAgent
title: IInstallationAgent (wuapi.h)
description: Records the result for an update.
helpviewer_keywords: ["IInstallationAgent","IInstallationAgent interface [Windows Update Agent]","IInstallationAgent interface [Windows Update Agent]","described","wua.iinstallationagent","wuapi/IInstallationAgent"]
old-location: wua\iinstallationagent.htm
tech.root: Wua_Sdk
ms.assetid: B24B527C-D92B-4BEB-ADCC-5E2BA684A478
ms.date: 12/05/2018
ms.keywords: IInstallationAgent, IInstallationAgent interface [Windows Update Agent], IInstallationAgent interface [Windows Update Agent],described, wua.iinstallationagent, wuapi/IInstallationAgent
f1_keywords:
- wuapi/IInstallationAgent
dev_langs:
- c++
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
- IInstallationAgent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInstallationAgent interface


## -description


Records the result for an update.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInstallationAgent</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IInstallationAgent</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iinstallationagent-recordinstallationresult">RecordInstallationResult</a>
</td>
<td align="left" width="63%">
Records the result for an update. The result is specified by an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-istringcollection">IStringCollection</a> object.

</td>
</tr>
</table> 

