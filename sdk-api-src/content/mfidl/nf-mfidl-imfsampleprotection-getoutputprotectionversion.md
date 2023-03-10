---
UID: NF:mfidl.IMFSampleProtection.GetOutputProtectionVersion
title: IMFSampleProtection::GetOutputProtectionVersion (mfidl.h)
description: Retrieves the version of sample protection that the component implements on output.
helpviewer_keywords: ["607e6123-0cfa-4946-b390-1c44e502b2db","GetOutputProtectionVersion","GetOutputProtectionVersion method [Media Foundation]","GetOutputProtectionVersion method [Media Foundation]","IMFSampleProtection interface","IMFSampleProtection interface [Media Foundation]","GetOutputProtectionVersion method","IMFSampleProtection.GetOutputProtectionVersion","IMFSampleProtection::GetOutputProtectionVersion","mf.imfsampleprotection_getoutputprotectionversion","mfidl/IMFSampleProtection::GetOutputProtectionVersion"]
old-location: mf\imfsampleprotection_getoutputprotectionversion.htm
tech.root: mf
ms.assetid: 607e6123-0cfa-4946-b390-1c44e502b2db
ms.date: 12/05/2018
ms.keywords: 607e6123-0cfa-4946-b390-1c44e502b2db, GetOutputProtectionVersion, GetOutputProtectionVersion method [Media Foundation], GetOutputProtectionVersion method [Media Foundation],IMFSampleProtection interface, IMFSampleProtection interface [Media Foundation],GetOutputProtectionVersion method, IMFSampleProtection.GetOutputProtectionVersion, IMFSampleProtection::GetOutputProtectionVersion, mf.imfsampleprotection_getoutputprotectionversion, mfidl/IMFSampleProtection::GetOutputProtectionVersion
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
 - IMFSampleProtection::GetOutputProtectionVersion
 - mfidl/IMFSampleProtection::GetOutputProtectionVersion
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
 - IMFSampleProtection.GetOutputProtectionVersion
---

# IMFSampleProtection::GetOutputProtectionVersion


## -description

Retrieves the version of sample protection that the component implements on output.

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