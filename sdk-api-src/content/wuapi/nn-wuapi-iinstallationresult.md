---
UID: NN:wuapi.IInstallationResult
title: IInstallationResult (wuapi.h)
description: Represents the result of an installation or uninstallation.
helpviewer_keywords: ["IInstallationResult","IInstallationResult interface [Windows Update Agent]","IInstallationResult interface [Windows Update Agent]","described","wua.iinstallationresult","wuapi/IInstallationResult"]
old-location: wua\iinstallationresult.htm
tech.root: Wua_Sdk
ms.assetid: 453945d7-11a3-4237-b1c8-928194be558d
ms.date: 12/05/2018
ms.keywords: IInstallationResult, IInstallationResult interface [Windows Update Agent], IInstallationResult interface [Windows Update Agent],described, wua.iinstallationresult, wuapi/IInstallationResult
f1_keywords:
- wuapi/IInstallationResult
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
- IInstallationResult
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInstallationResult interface


## -description


Represents the result of an installation or uninstallation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInstallationResult</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IInstallationResult</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInstallationResult</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iinstallationresult-getupdateresult">GetUpdateResult</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdateinstallationresult">IUpdateInstallationResult</a> interface that contains the installation results for a specified update.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInstallationResult</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iinstallationresult-get_hresult">HResult</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the <b>HRESULT</b> of the exception, if any, that is raised during the installation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iinstallationresult-get_rebootrequired">RebootRequired</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether you must restart the computer to complete the installation or uninstallation of an update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iinstallationresult-get_resultcode">ResultCode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/ne-wuapi-operationresultcode">OperationResultCode</a> value that specifies the result of an operation on an update.

</td>
</tr>
</table> 

