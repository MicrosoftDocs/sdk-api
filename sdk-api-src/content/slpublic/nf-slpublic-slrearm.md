---
UID: NF:slpublic.SLReArm
title: SLReArm function (slpublic.h)
author: windows-sdk-content
description: This function is rearm application activation.
old-location: security\slrearm.htm
tech.root: SecSLApi
ms.assetid: d1b47613-1e1d-4873-93ed-8ef2bc836c30
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SLReArm, SLReArm function [Security], security.slrearm, slpublic/SLReArm
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
 - SLReArm
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SLReArm function


## -description


This function is rearm application activation.


## -parameters




### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.


### -param pApplicationId [in]

Type: <b>const SLID*</b>

A pointer to the application ID.


### -param pProductSkuId [in, optional]

Type: <b>const SLID*</b>

A pointer to the product SKU ID.


### -param dwFlags [in]

Type: <b>DWORD</b>

Flags for ReArm behavior.  Valid values are 0 or          
		<b>SL_REARM_REBOOT_REQUIRED</b>.  Passing <b>SL_REARM_REBOOT_REQUIRED</b> will       
		require a reboot before a function using the security processor can     
		succeed.


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
 



