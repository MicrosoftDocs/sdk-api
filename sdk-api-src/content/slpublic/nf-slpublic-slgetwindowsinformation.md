---
UID: NF:slpublic.SLGetWindowsInformation
title: SLGetWindowsInformation function (slpublic.h)
description: Retrieves the value portion of a name-value pair from the licensing policy of a software component.
helpviewer_keywords: ["SLGetWindowsInformation","SLGetWindowsInformation function [Security]","security.slgetwindowsinformation","slpublic/SLGetWindowsInformation"]
old-location: security\slgetwindowsinformation.htm
tech.root: security
ms.assetid: 007b3f3a-c320-4bbc-ab5c-746b513cb815
ms.date: 12/05/2018
ms.keywords: SLGetWindowsInformation, SLGetWindowsInformation function [Security], security.slgetwindowsinformation, slpublic/SLGetWindowsInformation
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
 - SLGetWindowsInformation
 - slpublic/SLGetWindowsInformation
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
 - SLGetWindowsInformation
---

# SLGetWindowsInformation function


## -description

Retrieves the value portion of a name-value pair from the licensing policy of a software component.

## -parameters

### -param pwszValueName [in]

A pointer to a null-terminated string that contains the name associated with the value to retrieve.

### -param peDataType [out, optional]

A pointer to a value of the <a href="/windows/desktop/api/slpublic/ne-slpublic-sldatatype">SLDATATYPE</a> enumeration that specifies the type of data in the <i>ppbValue</i> buffer.

### -param pcbValue [out]

A pointer to the size, in bytes, of the <i>ppbValue</i> buffer.

### -param ppbValue [out]

A pointer to an array of <b>BYTE</b> pointers that specifies the value associated with the name specified by the <i>pwszValueName</i> parameter.

When you have finished using this array, free it by calling the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

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
<dt><b>SL_E_VALUE_NOT_FOUND</b></dt>
<dt>0xC004F012</dt>
</dl>
</td>
<td width="60%">
The specified name-value pair was not found.

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
The caller does not have the permissions necessary to call this function.

</td>
</tr>
</table>