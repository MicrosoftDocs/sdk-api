---
UID: NF:slpublic.SLSetGenuineInformation
title: SLSetGenuineInformation function (slpublic.h)
description: Specifies information about the genuine status of a Windows computer. (SLSetGenuineInformation)
helpviewer_keywords: ["SLSetGenuineInformation","SLSetGenuineInformation function [Security]","SL_BRT_COMMIT","SL_BRT_DATA","security.slsetgenuineinformation","slpublic/SLSetGenuineInformation"]
old-location: security\slsetgenuineinformation.htm
tech.root: security
ms.assetid: 20b82813-4c6e-4be8-969f-e6ed1fd5d008
ms.date: 12/05/2018
ms.keywords: SLSetGenuineInformation, SLSetGenuineInformation function [Security], SL_BRT_COMMIT, SL_BRT_DATA, security.slsetgenuineinformation, slpublic/SLSetGenuineInformation
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
 - SLSetGenuineInformation
 - slpublic/SLSetGenuineInformation
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
 - SLSetGenuineInformation
---

# SLSetGenuineInformation function


## -description

Specifies information about the genuine status of a Windows computer.

## -parameters

### -param pQueryId [in]

A pointer to an <b>SLID</b> structure that specifies the application for which to set information.

### -param pwszValueName [in]

A pointer to a null-terminated string that contains the name associated with the value to set. The following names are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SL_BRT_DATA"></a><a id="sl_brt_data"></a><dl>
<dt><b>SL_BRT_DATA</b></dt>
</dl>
</td>
<td width="60%">
Set information about the genuine state of the computer.

</td>
</tr>
<tr>
<td width="40%"><a id="SL_BRT_COMMIT"></a><a id="sl_brt_commit"></a><dl>
<dt><b>SL_BRT_COMMIT</b></dt>
</dl>
</td>
<td width="60%">
If the <b>SL_BRT_DATA</b> value  is set, setting <b>SL_BRT_COMMIT</b> puts the computer in nongenuine grace period mode.

</td>
</tr>
</table>

### -param eDataType [in]

A pointer to a value of the <a href="/windows/desktop/api/slpublic/ne-slpublic-sldatatype">SLDATATYPE</a> enumeration that specifies the type of data in the <i>pbValue</i> buffer.

### -param cbValue [in, optional]

A pointer to the size, in bytes, of the <i>pbValue</i> buffer.

### -param pbValue [in, optional]

A pointer to an array of <b>BYTE</b> values that specify the value associated with the name specified by the <i>pwszValueName</i> parameter.

Some name-value pairs allow this parameter to be <b>NULL</b>. In this case, the existing value of the name-value pair is deleted.

When you have finished using this array, free it by calling the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

This function can return the following values defined in Winerror.h and Slerror.h.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESS_DENIED</b></dt>
<dt>0x80070005</dt>
</dl>
</td>
<td width="60%">
The caller does not have administrative privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80000003</dt>
</dl>
</td>
<td width="60%">
The <i>pbValue</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>(HRESULT_FROM_WIN32)ERROR_BUFFER_OVERFLOW</b></dt>
<dt>0x111</dt>
</dl>
</td>
<td width="60%">
The <i>pbValue</i> buffer is too small to hold the data.

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
The data type of the <i>pbValue</i> parameter does not match the type specified by the <i>eDataType</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_DEPENDENT_PROPERTY_NOT_SET</b></dt>
<dt>0xC004F066</dt>
</dl>
</td>
<td width="60%">
The specified name-value pair is dependent on a name-value pair that has not been set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_NOT_SUPPORTED</b></dt>
<dt>0xC004F016</dt>
</dl>
</td>
<td width="60%">
The name specified by the <i>pwszValueName</i> parameter is not supported.

</td>
</tr>
</table>
