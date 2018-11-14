---
UID: NF:slpublic.SLPersistApplicationPolicies
title: SLPersistApplicationPolicies function
author: windows-sdk-content
description: Stores the current consumed policies to disk for fast policy access.
old-location: security\slpersistapplicationpolicies.htm
tech.root: SecSLApi
ms.assetid: a4bf2bcc-3ea5-4288-9bad-b74efdd9969c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SLPersistApplicationPolicies, SLPersistApplicationPolicies function [Security], security.slpersistapplicationpolicies, slpublic/SLPersistApplicationPolicies
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
 - SLPersistApplicationPolicies
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SLPersistApplicationPolicies
: 
---

# SLPersistApplicationPolicies function


## -description


Stores the current consumed policies to disk for fast policy access.


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
</table>
 




## -remarks



If the internal consumption fails then any current cache data is deleted.   
	Subsequent calls to the <a href="https://msdn.microsoft.com/a0852c0c-3d7d-4cca-a30b-b413c653b284">SLLoadApplicationPolicies</a> function will return     
	<b>SL_E_APPLICATION_POLICIES_MISSING</b>.

The <b>SLPersistApplicationPolicies</b> function returns success if the policy update succeeds,   
	regardless of internal consumption results.



