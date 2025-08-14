---
UID: NF:slpublic.SLGetWindowsInformationDWORD
title: SLGetWindowsInformationDWORD function (slpublic.h)
description: Retrieves the DWORD value portion of a name-value pair from the licensing policy of a software component.
helpviewer_keywords: ["SLGetWindowsInformationDWORD","SLGetWindowsInformationDWORD function [Security]","security.slgetwindowsinformationdword","slpublic/SLGetWindowsInformationDWORD"]
old-location: security\slgetwindowsinformationdword.htm
tech.root: security
ms.assetid: 27f59d01-93d5-4bf8-aab2-77243431cc0c
ms.date: 12/05/2018
ms.keywords: SLGetWindowsInformationDWORD, SLGetWindowsInformationDWORD function [Security], security.slgetwindowsinformationdword, slpublic/SLGetWindowsInformationDWORD
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - SLGetWindowsInformationDWORD
 - slpublic/SLGetWindowsInformationDWORD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-security-slc-l1-1-0.dll
 - Slc.dll
api_name:
 - SLGetWindowsInformationDWORD
---

# SLGetWindowsInformationDWORD function


## -description

Retrieves the <b>DWORD</b> value portion of a name-value pair from the licensing policy of a software component.

## -parameters

### -param pwszValueName [in]

A pointer to a null-terminated string that contains the name associated with the value to retrieve.

### -param pdwValue [out]

A pointer to the value associated with the name specified by the <i>pwszValueName</i> parameter.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

This function can return the following values defined in Slerror.h.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_RIGHT_NOT_GRANTED</b></dt>
<dt>0xC004F013</dt>
</dl>
</td>
<td width="60%">
The caller does not have the permissions necessary to call this function.

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
The value portion of the name-value pair is not a <b>DWORD</b>.

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
The requested policy is not defined for the current device.

</td>
</tr>
</table>
