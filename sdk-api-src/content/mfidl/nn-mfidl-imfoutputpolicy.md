---
UID: NN:mfidl.IMFOutputPolicy
title: IMFOutputPolicy (mfidl.h)
description: Encapsulates a usage policy from an input trust authority (ITA).helpviewer_keywords: ["76af8e03-9584-4f4b-ab2c-8a0ff2c3485b","IMFOutputPolicy","IMFOutputPolicy interface [Media Foundation]","IMFOutputPolicy interface [Media Foundation]","described","mf.imfoutputpolicy","mfidl/IMFOutputPolicy"]
old-location: mf\imfoutputpolicy.htm
tech.root: medfound
ms.assetid: 76af8e03-9584-4f4b-ab2c-8a0ff2c3485b
ms.date: 12/05/2018
ms.keywords: 76af8e03-9584-4f4b-ab2c-8a0ff2c3485b, IMFOutputPolicy, IMFOutputPolicy interface [Media Foundation], IMFOutputPolicy interface [Media Foundation],described, mf.imfoutputpolicy, mfidl/IMFOutputPolicy
f1_keywords:
- mfidl/IMFOutputPolicy
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFOutputPolicy interface


## -description


Encapsulates a usage policy from an input trust authority (ITA). Output trust authorities (OTAs) use this interface to query which protection systems they are required to enforce by the ITA.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFOutputPolicy</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>. <b>IMFOutputPolicy</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas">GenerateRequiredSchemas</a>
</td>
<td align="left" width="63%">
Retrieves a list of the output protection systems that the OTA must enforce, along with configuration data for each protection system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-getminimumgrlversion">GetMinimumGRLVersion</a>
</td>
<td align="left" width="63%">
Retrieves the minimum version of the global revocation list (GRL) that must be enforced by the protected environment for this policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-getoriginatorid">GetOriginatorID</a>
</td>
<td align="left" width="63%">
Retrieves a GUID identifying the ITA that created this output policy object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

