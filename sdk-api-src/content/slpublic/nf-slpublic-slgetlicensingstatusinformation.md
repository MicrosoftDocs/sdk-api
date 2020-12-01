---
UID: NF:slpublic.SLGetLicensingStatusInformation
title: SLGetLicensingStatusInformation function (slpublic.h)
description: Gets the licensing status of the specified application or SKU.
helpviewer_keywords: ["SLGetLicensingStatusInformation","SLGetLicensingStatusInformation function [Security]","security.slgetlicensingstatusinformation","slpublic/SLGetLicensingStatusInformation"]
old-location: security\slgetlicensingstatusinformation.htm
tech.root: security
ms.assetid: d35e6f8d-a019-46e0-9755-51f670f4913e
ms.date: 12/05/2018
ms.keywords: SLGetLicensingStatusInformation, SLGetLicensingStatusInformation function [Security], security.slgetlicensingstatusinformation, slpublic/SLGetLicensingStatusInformation
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
 - SLGetLicensingStatusInformation
 - slpublic/SLGetLicensingStatusInformation
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
 - SLGetLicensingStatusInformation
---

# SLGetLicensingStatusInformation function


## -description

Gets the  licensing status of the specified application or SKU.

## -parameters

### -param hSLC [in]

Type: <b>HSLC</b>

Handle to the current SLC context.

### -param pAppID [in, optional]

Type: <b>const SLID*</b>

A pointer to a <b>SLID</b> that represents the application ID.
		

<table>
<tr>
<th>pAppID</th>
<th>pProductSkuId</th>
<th>Results</th>
</tr>
<tr>
<td>
<b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
<td>
Get previous right consumption result.

</td>
</tr>
<tr>
<td>
<b>NULL</b>

</td>
<td>
Not <b>NULL</b>

</td>
<td>
Get licensing status of this SKU.

</td>
</tr>
<tr>
<td>
Not <b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
<td>
Get licensing status of this application.

</td>
</tr>
<tr>
<td>
Not <b>NULL</b>

</td>
<td>
Not <b>NULL</b>

</td>
<td>
Get licensing status of this application/SKU.

</td>
</tr>
</table>

### -param pProductSkuId [in, optional]

Type: <b>const SLID*</b>

A pointer to a <b>SLID</b> that represents the product ID.
		

<table>
<tr>
<th>pAppID</th>
<th>pProductSkuId</th>
<th>Results</th>
</tr>
<tr>
<td>
<b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
<td>
Get previous right consumption result.

</td>
</tr>
<tr>
<td>
<b>NULL</b>

</td>
<td>
Not <b>NULL</b>

</td>
<td>
Get licensing status of this SKU.

</td>
</tr>
<tr>
<td>
Not <b>NULL</b>

</td>
<td>
<b>NULL</b>

</td>
<td>
Get licensing status of this application.

</td>
</tr>
<tr>
<td>
Not <b>NULL</b>

</td>
<td>
Not <b>NULL</b>

</td>
<td>
Get licensing status of this application/SKU.

</td>
</tr>
</table>

### -param pwszRightName [in, optional]

Type: <b>PCWSTR</b>

Must be <b>NULL</b>.

### -param pnStatusCount [out]

Type: <b>UINT*</b>

A pointer to the number of the SKU's status.

### -param ppLicensingStatus [out]

Type: <b><a href="/windows/desktop/api/slpublic/ns-slpublic-sl_licensing_status">SL_LICENSING_STATUS</a>**</b>

A pointer to the licensing status of the SKU.

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
<dt><b>SL_E_RIGHT_NOT_CONSUMED</b></dt>
<dt>0xC004F002</dt>
</dl>
</td>
<td width="60%">
The rights consumption failed.

</td>
</tr>
</table>