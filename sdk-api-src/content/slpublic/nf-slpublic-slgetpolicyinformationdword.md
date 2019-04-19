---
UID: NF:slpublic.SLGetPolicyInformationDWORD
title: SLGetPolicyInformationDWORD function (slpublic.h)
author: windows-sdk-content
description: Gets the policy information after right has been consumed successfully.
old-location: security\slgetpolicyinformationdword.htm
tech.root: SecSLApi
ms.assetid: 273e843d-94eb-405d-b7fa-43d49783282f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SLGetPolicyInformationDWORD, SLGetPolicyInformationDWORD function [Security], security.slgetpolicyinformationdword, slpublic/SLGetPolicyInformationDWORD
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
req.lib: Slc.lib
req.dll: Slc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Slc.dll
api_name:
 - SLGetPolicyInformationDWORD
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SLGetPolicyInformationDWORD function


## -description


Gets the policy information after right has been consumed successfully.


## -parameters




### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.


### -param pwszValueName [in]

Type: <b>PCWSTR</b>

The policy name.


### -param pdwValue [out]

Type: <b>DWORD*</b>

A pointer to the return value.


## -returns



Type: <b>HRESULT WINAPI</b>

If this function succeeds, it return <b>S_OK</b>.  Otherwise, it returns an <b>HRESULT</b> error code.

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
<dt><b>SL_E_VALUE_NOT_FOUND</b></dt>
<dt>0xC004F012</dt>
</dl>
</td>
<td width="60%">
The value for the input key was not found.

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
<dt><b>SL_E_DATATYPE_MISMATCHED</b></dt>
<dt>0xC004F01E</dt>
</dl>
</td>
<td width="60%">
The input data type does not match the data type in the license.


</td>
</tr>
</table>
 



