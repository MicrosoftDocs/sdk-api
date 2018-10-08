---
UID: NN:mfidl.IMFTrustedInput
title: IMFTrustedInput
author: windows-sdk-content
description: Implemented by components that provide input trust authorities (ITAs). This interface is used to get the ITA for each of the component's streams.
old-location: mf\imftrustedinput.htm
tech.root: medfound
ms.assetid: 59a9def7-69a6-4f80-bb5e-1cb372ff6eab
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: 59a9def7-69a6-4f80-bb5e-1cb372ff6eab, IMFTrustedInput, IMFTrustedInput interface [Media Foundation], IMFTrustedInput interface [Media Foundation],described, mf.imftrustedinput, mfidl/IMFTrustedInput
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTrustedInput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTrustedInput interface


## -description


Implemented by components that provide input trust authorities (ITAs). This interface is used to get the ITA for each of the component's streams.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTrustedInput</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFTrustedInput</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTrustedInput</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4ebf02e-554a-4e7e-93d3-6f37d8b689bf">GetInputTrustAuthority</a>
</td>
<td align="left" width="63%">
Retrieves the ITA for a specified stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

