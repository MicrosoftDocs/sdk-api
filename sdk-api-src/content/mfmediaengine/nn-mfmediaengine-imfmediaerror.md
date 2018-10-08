---
UID: NN:mfmediaengine.IMFMediaError
title: IMFMediaError
author: windows-sdk-content
description: Provides the current error status for the Media Engine.
old-location: mf\imfmediaerror.htm
tech.root: medfound
ms.assetid: 08F161FE-C0E5-44EE-923E-646ADA534C42
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IMFMediaError, IMFMediaError interface [Media Foundation], IMFMediaError interface [Media Foundation],described, mf.imfmediaerror, mfmediaengine/IMFMediaError
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaError interface


## -description


Provides the current error status for the Media Engine.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaError</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaError</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaError</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6E4C4559-F59C-488C-A790-D95831BC9D29">GetErrorCode</a>
</td>
<td align="left" width="63%">
Gets the error code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73B414F2-F17E-418E-9F8B-A7C378F80090">GetExtendedErrorCode</a>
</td>
<td align="left" width="63%">
Gets the extended error code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0CEFC8A5-CCEA-43CF-80AB-C9862B0DAEDA">SetErrorCode</a>
</td>
<td align="left" width="63%">
Sets the error code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F3B52C1A-E235-492D-93C2-393FF2321B7E">SetExtendedErrorCode</a>
</td>
<td align="left" width="63%">
Sets the extended error code.

</td>
</tr>
</table> 


## -remarks



The <b>IMFMediaError</b> interface corresponds to the <b>MediaError</b> object in HTML5.

To get a pointer to this interface, call <a href="https://msdn.microsoft.com/F8A51AF8-8D73-47BC-ADA2-7F5108587873">IMFMediaEngine::GetError</a>.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

