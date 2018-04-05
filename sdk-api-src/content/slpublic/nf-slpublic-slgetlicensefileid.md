---
UID: NF:slpublic.SLGetLicenseFileId
title: SLGetLicenseFileId function
author: windows-driver-content
description: Checks if the license BLOB has been installed already.
old-location: security\slgetlicensefileid.htm
old-project: SecSLApi
ms.assetid: b8474a25-2aef-43b6-85be-71dc287fd712
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: SLGetLicenseFileId, SLGetLicenseFileId function [Security], security.slgetlicensefileid, slpublic/SLGetLicenseFileId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: SL_ACTIVATION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Slc.dll
api_name:
-	SLGetLicenseFileId
product: Windows
targetos: Windows
req.lib: Slc.lib
req.dll: Slc.dll
req.irql: 
req.product: Internet Explorer 6.01
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
 



