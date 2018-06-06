---
UID: NF:slpublic.SLLoadApplicationPolicies
title: SLLoadApplicationPolicies function
author: windows-sdk-content
description: Loads the application policies set with the SLPersistApplicationPolicies function for use by the SLGetApplicationPolicy function.
old-location: security\slloadapplicationpolicies.htm
old-project: SecSLApi
ms.assetid: a0852c0c-3d7d-4cca-a30b-b413c653b284
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: SLLoadApplicationPolicies, SLLoadApplicationPolicies function [Security], security.slloadapplicationpolicies, slpublic/SLLoadApplicationPolicies
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
 - SLLoadApplicationPolicies
product: Windows
targetos: Windows
req.lib: Slc.lib
req.dll: Slc.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SLLoadApplicationPolicies function


## -description


Loads the application policies set with the <a href="https://msdn.microsoft.com/a4bf2bcc-3ea5-4288-9bad-b74efdd9969c">SLPersistApplicationPolicies</a> function   
	for use by the <a href="https://msdn.microsoft.com/4d4b30bb-8548-4656-9fd9-553e8f8fb248">SLGetApplicationPolicy</a> function.


## -parameters




### -param pApplicationId [in]

Type: <b>const SLID*</b>

A pointer to the identifier of the application ID to be used for the fast policy queries.


### -param pProductSkuId [in, optional]

Type: <b>const SLID*</b>

A pointer to the identifier of the ACID to be used for the fast policy queries.


### -param dwFlags [in]

Type: <b>DWORD</b>

Additional flags.


### -param phPolicyContext [out]

Type: <b>HSLP*</b>

A pointer to a policy context for use in the <a href="https://msdn.microsoft.com/4d4b30bb-8548-4656-9fd9-553e8f8fb248">SLGetApplicationPolicy</a> function and    
		the <a href="https://msdn.microsoft.com/56dae943-659a-4e75-81ef-0d58fa3cd6d2">SLUnloadApplicationPolicies</a> function.


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
<dt><b>SL_E_APPLICATION_POLICIES_MISSING</b></dt>
<dt>0xC004F072</dt>
</dl>
</td>
<td width="60%">
The license policies for fast query could not be found.

</td>
</tr>
</table>
 



