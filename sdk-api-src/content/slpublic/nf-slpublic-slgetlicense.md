---
UID: NF:slpublic.SLGetLicense
title: SLGetLicense function
author: windows-sdk-content
description: Returns the license file BLOB.
old-location: security\slgetlicense.htm
old-project: SecSLApi
ms.assetid: 68648512-ea63-43b9-af86-b1014c89f1d7
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: SLGetLicense, SLGetLicense function [Security], security.slgetlicense, slpublic/SLGetLicense
ms.prod: windows
ms.technology: windows-sdk
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
-	SLGetLicense
product: Windows
targetos: Windows
req.lib: Slc.lib
req.dll: Slc.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SLGetLicense function


## -description


Returns the license file BLOB.


## -parameters




### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.


### -param pLicenseFileId [in]

Type: <b>const SLID*</b>

A pointer to the license file ID.


### -param pcbLicenseFile [out]

Type: <b>UINT*</b>

A pointer to the size, in bytes, of the license file BLOB.


### -param ppbLicenseFile [out]

Type: <b>PBYTE*</b>

The license file BLOB.


## -returns



Type: <b>HRESULT WINAPI</b>

If this function succeeds, it return <b>S_OK</b>.  Otherwise,  it returns an <b>HRESULT</b> error code.

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
<dt><b>SL_E_LICENSE_FILE_NOT_INSTALLED</b></dt>
<dt>0xC004F011</dt>
</dl>
</td>
<td width="60%">
The license file is not installed.

</td>
</tr>
</table>
 



