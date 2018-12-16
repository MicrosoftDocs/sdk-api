---
UID: NN:mfidl.IMFTrustedOutput
title: IMFTrustedOutput
author: windows-sdk-content
description: Implemented by components that provide output trust authorities (OTAs).
old-location: mf\imftrustedoutput.htm
tech.root: medfound
ms.assetid: 14342d8b-3c76-4c13-8cbe-a60bb66084c8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 14342d8b-3c76-4c13-8cbe-a60bb66084c8, IMFTrustedOutput, IMFTrustedOutput interface [Media Foundation], IMFTrustedOutput interface [Media Foundation],described, mf.imftrustedoutput, mfidl/IMFTrustedOutput
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
 - IMFTrustedOutput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFTrustedOutput interface


## -description


Implemented by components that provide output trust authorities (OTAs). Any Media Foundation transform (MFT) or media sink that is designed to work within the protected media path (PMP) and also sends protected content outside the Media Foundation pipeline must implement this interface.

The policy engine uses this interface to negotiate what type of content protection should be applied to the content. Applications do not use this interface directly.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTrustedOutput</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFTrustedOutput</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTrustedOutput</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4dd570e7-c6fb-4ffb-8ef5-b88a6638dbbf">GetOutputTrustAuthorityByIndex</a>
</td>
<td align="left" width="63%">
Gets an OTA, specified by index.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3aae6859-0b32-4705-9045-b98d0bbf43a6">GetOutputTrustAuthorityCount</a>
</td>
<td align="left" width="63%">
Gets the number of OTAs provided by this trusted output.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/085cac9c-f8c1-45b9-a8fe-c2c5cc941439">IsFinal</a>
</td>
<td align="left" width="63%">
Queries whether this output is a policy sink, meaning it handles the rights and restrictions required by the input trust authority (ITA).
        

</td>
</tr>
</table> 


## -remarks



If an MFT supports <b>IMFTrustedOutput</b>, it must expose the interface through <b>QueryInterface</b>. The interface applies to all of the input streams on the MFT. (There is no mechanism to return a separate <b>IMFTrustedOutput</b> pointer for each stream.) The MFT must apply the  output policies to all of its input streams. If the MFT sends different streams to separate connectors, it must report all of the connector attributes.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

