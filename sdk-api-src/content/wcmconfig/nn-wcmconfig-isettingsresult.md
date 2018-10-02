---
UID: NN:wcmconfig.ISettingsResult
title: ISettingsResult
author: windows-sdk-content
description: Retrieves the code and description for errors and warnings returned by various operations.
old-location: smi\isettingsresult.htm
tech.root: SMI
ms.assetid: 0bbfd39a-0292-4d8e-ae31-f45aebd326a7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISettingsResult, ISettingsResult interface [SMI], ISettingsResult interface [SMI],described, smi.isettingsresult, wcmconfig/ISettingsResult
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# ISettingsResult interface


## -description


Retrieves the code and description for errors and warnings returned by various operations.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISettingsResult</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISettingsResult</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/09e1c5ae-f5ba-4f5a-b35d-a1c2e8dbdfe9">GetColumn</a>
</td>
<td align="left" width="63%">
Returns the column number where the error has occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2bb39ce-9c49-46ab-b7d7-e4e4794f6b5a">GetContextDescription</a>
</td>
<td align="left" width="63%">
Returns the description of the context that surrounds the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d020bd46-8967-4105-856d-ee448b527852">GetDescription</a>
</td>
<td align="left" width="63%">
Returns the description of the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0044133-480e-4b40-ad3f-b3d65e259029">GetErrorCode</a>
</td>
<td align="left" width="63%">
Returns the HRESULT error code value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c74beea9-5e81-4cd2-ade2-c812b6a035a1">GetLine</a>
</td>
<td align="left" width="63%">
Returns the line number where the error has occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a76b243-5294-47a7-8ad3-b39425735866">GetSource</a>
</td>
<td align="left" width="63%">
Returns the file or path where the error has occurred.

</td>
</tr>
</table> 

