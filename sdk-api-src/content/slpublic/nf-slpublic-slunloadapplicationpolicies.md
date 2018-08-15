---
UID: NF:slpublic.SLUnloadApplicationPolicies
title: SLUnloadApplicationPolicies function
author: windows-sdk-content
description: Releases the policy context handle returned by the SLLoadApplicationPolicies function.
old-location: security\slunloadapplicationpolicies.htm
old-project: secslapi
ms.assetid: 56dae943-659a-4e75-81ef-0d58fa3cd6d2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SLUnloadApplicationPolicies, SLUnloadApplicationPolicies function [Security], security.slunloadapplicationpolicies, slpublic/SLUnloadApplicationPolicies
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: slpublic.h
req.include-header: 
req.redist: 
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
 - SLUnloadApplicationPolicies
product: Windows
targetos: Windows
req.lib: Slc.lib
req.dll: Slc.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SLUnloadApplicationPolicies function


## -description


Releases the policy context handle returned by the <a href="https://msdn.microsoft.com/a0852c0c-3d7d-4cca-a30b-b413c653b284">SLLoadApplicationPolicies</a> function.


## -parameters




### -param hPolicyContext [in]

Type: <b>HSLP</b>

The context handle returned by the <a href="https://msdn.microsoft.com/a0852c0c-3d7d-4cca-a30b-b413c653b284">SLLoadApplicationPolicies</a> function.


### -param dwFlags [in]

Type: <b>DWORD</b>

The additional flags.


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
<dt><b>SL_E_APPLICATION_POLICIES_NOT_LOADED</b></dt>
<dt>0xC004F073</dt>
</dl>
</td>
<td width="60%">
The policy context was not found.

</td>
</tr>
</table>
 



