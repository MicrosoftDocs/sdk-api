---
UID: NN:mfidl.IMFOutputPolicy
title: IMFOutputPolicy
author: windows-sdk-content
description: Encapsulates a usage policy from an input trust authority (ITA).
old-location: mf\imfoutputpolicy.htm
tech.root: medfound
ms.assetid: 76af8e03-9584-4f4b-ab2c-8a0ff2c3485b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 76af8e03-9584-4f4b-ab2c-8a0ff2c3485b, IMFOutputPolicy, IMFOutputPolicy interface [Media Foundation], IMFOutputPolicy interface [Media Foundation],described, mf.imfoutputpolicy, mfidl/IMFOutputPolicy
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
 - IMFOutputPolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFOutputPolicy interface


## -description


Encapsulates a usage policy from an input trust authority (ITA). Output trust authorities (OTAs) use this interface to query which protection systems they are required to enforce by the ITA.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFOutputPolicy</b> interface inherits from <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>. <b>IMFOutputPolicy</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFOutputPolicy</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23f5f0df-e2cc-4593-8c3e-dca3638161e2">GenerateRequiredSchemas</a>
</td>
<td align="left" width="63%">
Retrieves a list of the output protection systems that the OTA must enforce, along with configuration data for each protection system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41da430b-9cdd-4ab0-873d-f6d94f48d401">GetMinimumGRLVersion</a>
</td>
<td align="left" width="63%">
Retrieves the minimum version of the global revocation list (GRL) that must be enforced by the protected environment for this policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3412bb81-c4b8-4e10-9a8e-8eae413ca82d">GetOriginatorID</a>
</td>
<td align="left" width="63%">
Retrieves a GUID identifying the ITA that created this output policy object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

