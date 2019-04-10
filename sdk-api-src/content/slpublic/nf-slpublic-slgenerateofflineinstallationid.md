---
UID: NF:slpublic.SLGenerateOfflineInstallationId
title: SLGenerateOfflineInstallationId function (slpublic.h)
author: windows-sdk-content
description: Generates the Installation ID (IID).
old-location: security\slgenerateofflineinstallationid.htm
tech.root: SecSLApi
ms.assetid: 2bfbedfc-6fac-468b-8314-c856aab856d0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SLGenerateOfflineInstallationId, SLGenerateOfflineInstallationId function [Security], security.slgenerateofflineinstallationid, slpublic/SLGenerateOfflineInstallationId
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
 - SLGenerateOfflineInstallationId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SLGenerateOfflineInstallationId function


## -description


Generates the  Installation ID (IID).    
	 Users can send the IID to CSR to get the Confirmation ID (CID).


## -parameters




### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.


### -param pProductSkuId [in]

Type: <b>const SLID*</b>

A pointer to the product ID.


### -param ppwszInstallationId [out]

Type: <b>PWSTR*</b>

The Installation ID string. Once you are finished, call the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function to      
		free the memory.


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
<dt><b>SL_E_PKEY_NOT_INSTALLED</b></dt>
<dt>0xC004F014</dt>
</dl>
</td>
<td width="60%">
The product key is not available.

</td>
</tr>
</table>
 



