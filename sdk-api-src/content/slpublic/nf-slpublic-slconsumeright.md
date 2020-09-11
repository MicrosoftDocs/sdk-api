---
UID: NF:slpublic.SLConsumeRight
title: SLConsumeRight function (slpublic.h)
description: Let an application to exercise rights on a locally-stored licenses.
helpviewer_keywords: ["SLConsumeRight","SLConsumeRight function [Security]","security.slconsumeright","slpublic/SLConsumeRight"]
old-location: security\slconsumeright.htm
tech.root: security
ms.assetid: d61ec4ec-c552-4963-8f4e-a1540081e747
ms.date: 12/05/2018
ms.keywords: SLConsumeRight, SLConsumeRight function [Security], security.slconsumeright, slpublic/SLConsumeRight
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
 - SLConsumeRight
 - slpublic/SLConsumeRight
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
 - SLConsumeRight
---

# SLConsumeRight function


## -description

Let an application to exercise rights on a locally-stored licenses. Calling this function binds a license to the right.

## -parameters

### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.

### -param pAppId [in]

Type: <b>const SLID*</b>

A pointer to the identifier of the application who's right is going to be          
		consumed.

### -param pProductSkuId [in, optional]

Type: <b>const SLID*</b>

A pointer to the identifier of product SKU. If set to <b>NULL</b>, all of the  product  SKU's          
		licenses will be consumed.

### -param pwszRightName [in, optional]

Type: <b>PCWSTR</b>

The name of right to be consumed.

### -param pvReserved

Type: <b>PVOID</b>

Reserved.

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
<dt><b>SL_E_RIGHT_NOT_GRANTED</b></dt>
<dt>0xC004F013</dt>
</dl>
</td>
<td width="60%">
The caller does not have permission to run the software.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_PRODUCT_SKU_NOT_INSTALLED </b></dt>
<dt>0xC004F015</dt>
</dl>
</td>
<td width="60%">
The license is not installed.

</td>
</tr>
</table>

