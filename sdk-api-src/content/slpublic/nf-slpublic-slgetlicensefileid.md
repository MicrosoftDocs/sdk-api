---
UID: NF:slpublic.SLGetLicenseFileId
title: SLGetLicenseFileId function (slpublic.h)
description: Checks if the license BLOB has been installed already.
helpviewer_keywords: ["SLGetLicenseFileId","SLGetLicenseFileId function [Security]","security.slgetlicensefileid","slpublic/SLGetLicenseFileId"]
old-location: security\slgetlicensefileid.htm
tech.root: security
ms.assetid: b8474a25-2aef-43b6-85be-71dc287fd712
ms.date: 12/05/2018
ms.keywords: SLGetLicenseFileId, SLGetLicenseFileId function [Security], security.slgetlicensefileid, slpublic/SLGetLicenseFileId
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Slc.lib
req.dll: Slc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SLGetLicenseFileId
 - slpublic/SLGetLicenseFileId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Slc.dll
api_name:
 - SLGetLicenseFileId
---

# SLGetLicenseFileId function


## -description

Checks if the license BLOB has been 
	installed already.

## -parameters

### -param hSLC [in]

The handle to the current SLC context.

### -param cbLicenseBlob [in]

The size, in bytes, of the license BLOB.

### -param pbLicenseBlob [in]

A pointer to the number of licenses in the BLOB.

### -param pLicenseFileId [out]

A pointer to the license file ID.

## -returns

If the License has been previously installed, it returns a <b>SLID</b>.  Otherwise,  it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_INVALID_LICENSE</b></dt>
<dt>0xC004F01F</dt>
</dl>
</td>
<td width="60%">
The license is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_LICENSE_FILE_NOT_INSTALLED</b></dt>
<dt>0xC004F011</dt>
</dl>
</td>
<td width="60%">
The license file is not installed.

</td>
</tr>
</table>

