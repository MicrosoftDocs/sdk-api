---
UID: NF:mfidl.IMFSampleProtection.GetInputProtectionVersion
title: IMFSampleProtection::GetInputProtectionVersion (mfidl.h)
description: Retrieves the version of sample protection that the component implements on input.
helpviewer_keywords: ["26f92775-f8a0-4b85-8cfc-353349325706","GetInputProtectionVersion","GetInputProtectionVersion method [Media Foundation]","GetInputProtectionVersion method [Media Foundation]","IMFSampleProtection interface","IMFSampleProtection interface [Media Foundation]","GetInputProtectionVersion method","IMFSampleProtection.GetInputProtectionVersion","IMFSampleProtection::GetInputProtectionVersion","mf.imfsampleprotection_getinputprotectionversion","mfidl/IMFSampleProtection::GetInputProtectionVersion"]
old-location: mf\imfsampleprotection_getinputprotectionversion.htm
tech.root: mf
ms.assetid: 26f92775-f8a0-4b85-8cfc-353349325706
ms.date: 12/05/2018
ms.keywords: 26f92775-f8a0-4b85-8cfc-353349325706, GetInputProtectionVersion, GetInputProtectionVersion method [Media Foundation], GetInputProtectionVersion method [Media Foundation],IMFSampleProtection interface, IMFSampleProtection interface [Media Foundation],GetInputProtectionVersion method, IMFSampleProtection.GetInputProtectionVersion, IMFSampleProtection::GetInputProtectionVersion, mf.imfsampleprotection_getinputprotectionversion, mfidl/IMFSampleProtection::GetInputProtectionVersion
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
 - IMFSampleProtection::GetInputProtectionVersion
 - mfidl/IMFSampleProtection::GetInputProtectionVersion
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
 - IMFSampleProtection.GetInputProtectionVersion
---

# IMFSampleProtection::GetInputProtectionVersion


## -description

Retrieves the version of sample protection that the component implements on input.

## -parameters

### -param pdwVersion [out]

Receives a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-sample_protection_version">SAMPLE_PROTECTION_VERSION</a> enumeration.

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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsampleprotection">IMFSampleProtection</a>