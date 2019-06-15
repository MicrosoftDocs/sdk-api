---
UID: NN:wcmconfig.ISettingsResult
title: ISettingsResult (wcmconfig.h)
author: windows-sdk-content
description: Retrieves the code and description for errors and warnings returned by various operations.
old-location: smi\isettingsresult.htm
tech.root: SMI
ms.assetid: 0bbfd39a-0292-4d8e-ae31-f45aebd326a7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISettingsResult, ISettingsResult interface [SMI], ISettingsResult interface [SMI],described, smi.isettingsresult, wcmconfig/ISettingsResult
ms.topic: interface
f1_keywords: ["wcmconfig/ISettingsResult"]
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISettingsResult interface


## -description


Retrieves the code and description for errors and warnings returned by various operations.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISettingsResult</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISettingsResult</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISettingsResult</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsresult-getcolumn">GetColumn</a>
</td>
<td align="left" width="63%">
Returns the column number where the error has occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsresult-getcontextdescription">GetContextDescription</a>
</td>
<td align="left" width="63%">
Returns the description of the context that surrounds the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsresult-getdescription">GetDescription</a>
</td>
<td align="left" width="63%">
Returns the description of the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsresult-geterrorcode">GetErrorCode</a>
</td>
<td align="left" width="63%">
Returns the HRESULT error code value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsresult-getline">GetLine</a>
</td>
<td align="left" width="63%">
Returns the line number where the error has occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsresult-getsource">GetSource</a>
</td>
<td align="left" width="63%">
Returns the file or path where the error has occurred.

</td>
</tr>
</table> 

