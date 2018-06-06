---
UID: NF:slpublic.SLGetApplicationPolicy
title: SLGetApplicationPolicy function
author: windows-sdk-content
description: Queries a policy from the set stored with the SLPersistApplicationPolicies function and loaded using the SLLoadApplicationPolicies function.
old-location: security\slgetapplicationpolicy.htm
old-project: SecSLApi
ms.assetid: 4d4b30bb-8548-4656-9fd9-553e8f8fb248
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: SLGetApplicationPolicy, SLGetApplicationPolicy function [Security], security.slgetapplicationpolicy, slpublic/SLGetApplicationPolicy
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
tech.root: 
req.typenames: SL_ACTIVATION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Slc.dll
api_name:
 - SLGetApplicationPolicy
product: Windows
targetos: Windows
req.lib: Slc.lib
req.dll: Slc.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SLGetApplicationPolicy function


## -description


Queries a policy from the set stored with the <a href="https://msdn.microsoft.com/a4bf2bcc-3ea5-4288-9bad-b74efdd9969c">SLPersistApplicationPolicies</a> function     
	and loaded using the <a href="https://msdn.microsoft.com/a0852c0c-3d7d-4cca-a30b-b413c653b284">SLLoadApplicationPolicies</a> function.


## -parameters




### -param hPolicyContext [in]

Type: <b>HSLP</b>

The context handle returned by the <a href="https://msdn.microsoft.com/a0852c0c-3d7d-4cca-a30b-b413c653b284">SLLoadApplicationPolicies</a> function.


### -param pwszValueName [in]

Type: <b>PCWSTR</b>

The name of the policy to query, or "*" for all policies.


### -param peDataType [out, optional]

Type: <b><a href="https://msdn.microsoft.com/245e79de-4823-4af9-926a-088e263cc802">SLDATATYPE</a>*</b>

A pointer to the type of the data, if available.


### -param pcbValue [out]

Type: <b>UINT*</b>

A pointer to  the size, in bytes, of the data, if  available.


### -param ppbValue [out]

Type: <b>PBYTE*</b>

 The data, if available.


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
<dt><b>SL_E_APPLICATION_POLICIES_NOT_LOADED</b></dt>
<dt>0xC004F073</dt>
</dl>
</td>
<td width="60%">
The policy context was not found.

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
The policy is not found.

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
The policy list is empty.

</td>
</tr>
</table>
 



