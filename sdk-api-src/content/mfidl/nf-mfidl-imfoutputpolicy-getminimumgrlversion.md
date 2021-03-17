---
UID: NF:mfidl.IMFOutputPolicy.GetMinimumGRLVersion
title: IMFOutputPolicy::GetMinimumGRLVersion (mfidl.h)
description: Retrieves the minimum version of the global revocation list (GRL) that must be enforced by the protected environment for this policy.
helpviewer_keywords: ["41da430b-9cdd-4ab0-873d-f6d94f48d401","GetMinimumGRLVersion","GetMinimumGRLVersion method [Media Foundation]","GetMinimumGRLVersion method [Media Foundation]","IMFOutputPolicy interface","IMFOutputPolicy interface [Media Foundation]","GetMinimumGRLVersion method","IMFOutputPolicy.GetMinimumGRLVersion","IMFOutputPolicy::GetMinimumGRLVersion","mf.imfoutputpolicy_getminimumgrlversion","mfidl/IMFOutputPolicy::GetMinimumGRLVersion"]
old-location: mf\imfoutputpolicy_getminimumgrlversion.htm
tech.root: mf
ms.assetid: 41da430b-9cdd-4ab0-873d-f6d94f48d401
ms.date: 12/05/2018
ms.keywords: 41da430b-9cdd-4ab0-873d-f6d94f48d401, GetMinimumGRLVersion, GetMinimumGRLVersion method [Media Foundation], GetMinimumGRLVersion method [Media Foundation],IMFOutputPolicy interface, IMFOutputPolicy interface [Media Foundation],GetMinimumGRLVersion method, IMFOutputPolicy.GetMinimumGRLVersion, IMFOutputPolicy::GetMinimumGRLVersion, mf.imfoutputpolicy_getminimumgrlversion, mfidl/IMFOutputPolicy::GetMinimumGRLVersion
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFOutputPolicy::GetMinimumGRLVersion
 - mfidl/IMFOutputPolicy::GetMinimumGRLVersion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFOutputPolicy.GetMinimumGRLVersion
---

# IMFOutputPolicy::GetMinimumGRLVersion


## -description

Retrieves the minimum version of the global revocation list (GRL) that must be enforced by the protected environment for this policy.

## -parameters

### -param pdwMinimumGRLVersion [out]

Receives the minimum GRL version.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy">IMFOutputPolicy</a>