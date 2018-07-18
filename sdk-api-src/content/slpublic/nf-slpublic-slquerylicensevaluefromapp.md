---
UID: NF:slpublic.SLQueryLicenseValueFromApp
title: SLQueryLicenseValueFromApp function
author: windows-sdk-content
description: Gets the value for the specified component policy.
old-location: security\slquerylicensevaluefromapp.htm
old-project: SecSLApi
ms.assetid: C26FF469-2B25-4EDA-8432-EF32A4550650
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: SLQueryLicenseValueFromApp, SLQueryLicenseValueFromApp function [Security], security.slquerylicensevaluefromapp, slpublic/SLQueryLicenseValueFromApp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - api-ms-win-core-slapi-l1-1-0.dll
 - Slc.dll
 - Clipc.dll
api_name:
 - SLQueryLicenseValueFromApp
product: Windows
targetos: Windows
req.lib: Api-ms-win-core-slapi-l1-1-0.lib
req.dll: Api-ms-win-core-slapi-l1-1-0.dll
req.irql: 
req.product: Outlook Express 6.0
---

# SLQueryLicenseValueFromApp function


## -description


<p class="CCE_Message">[This API is not available to all Windows/Windows Phone apps. Unless your developer account is specially provisioned by Microsoft, calls to these APIs will fail at runtime.]

Gets the value for the specified component policy.


## -parameters




### -param valueName [in]

The name of the policy for which you want to get information.


### -param valueType [out, optional]

The data type of the policy value. The following table describes the values that this parameter can 
       receive.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>REG_DWORD</td>
<td>A 32-bit integer.  For this type, the size of the buffer that the <i>dataBuffer</i> 
         parameter specifies should be at least 4 bytes.</td>
</tr>
<tr>
<td>REG_BINARY</td>
<td>A binary value.</td>
</tr>
<tr>
<td>REG_SZ</td>
<td>A wide-character, null-terminated string, including the last null character.</td>
</tr>
</table>
 


### -param dataBuffer [out, optional]

A buffer that receives the value of the component policy.


### -param dataSize [in]

The size of the supplied buffer, in bytes.


### -param resultDataSize [out]

The actual size of the data received for the policy value, in bytes.


## -returns



If this function succeeds, it return <b>S_OK</b>.  Otherwise, it returns an 
      <b>HRESULT</b> error code.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
The specified name-value pair was not found.

</td>
</tr>
</table>
 




## -remarks



Your app must have the restricted slapiQueryLicenseValue capability to call the <b>SLQueryLicenseValueFromApp</b> function.



