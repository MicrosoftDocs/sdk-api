---
UID: NF:bits.IBackgroundCopyError.GetErrorDescription
title: IBackgroundCopyError::GetErrorDescription (bits.h)
description: Retrieves the error text associated with the error.
helpviewer_keywords: ["GetErrorDescription","GetErrorDescription method [BITS]","GetErrorDescription method [BITS]","IBackgroundCopyError interface","IBackgroundCopyError interface [BITS]","GetErrorDescription method","IBackgroundCopyError.GetErrorDescription","IBackgroundCopyError::GetErrorDescription","_drz_ibackgroundcopyerror_geterrordescription","bits.ibackgroundcopyerror_geterrordescription","bits/IBackgroundCopyError::GetErrorDescription"]
old-location: bits\ibackgroundcopyerror_geterrordescription.htm
tech.root: Bits
ms.assetid: 57323f38-c2e6-4e40-b357-7df758899f97
ms.date: 12/05/2018
ms.keywords: GetErrorDescription, GetErrorDescription method [BITS], GetErrorDescription method [BITS],IBackgroundCopyError interface, IBackgroundCopyError interface [BITS],GetErrorDescription method, IBackgroundCopyError.GetErrorDescription, IBackgroundCopyError::GetErrorDescription, _drz_ibackgroundcopyerror_geterrordescription, bits.ibackgroundcopyerror_geterrordescription, bits/IBackgroundCopyError::GetErrorDescription
req.header: bits.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyError::GetErrorDescription
 - bits/IBackgroundCopyError::GetErrorDescription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyError.GetErrorDescription
---

# IBackgroundCopyError::GetErrorDescription


## -description

Retrieves the error text associated with the error.

## -parameters

### -param LanguageId [in]

Identifies the locale to use to generate the description. To create the language identifier, use the 
<a href="/windows/win32/api/winnt/nf-winnt-makelangid">MAKELANGID</a> macro. For example, to specify U.S. English, use the following code sample. 




<code>MAKELANGID(LANG_ENGLISH, SUBLANG_ENGLISH_US)</code>

To retrieve the system's default user language identifier, use the following calls.

<code>LANGIDFROMLCID(GetThreadLocale())</code>

### -param pErrorDescription [out]

Null-terminated string that contains the error text associated with the error. Call the 
<a href="/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to free <i>ppErrorDescription</i> when done.

## -returns

This method returns the following <b>HRESULT</b> values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Description of the error was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>LanguageId</i> parameter cannot be 0.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_RESOURCE_LANG_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
No string is available for the locale.

</td>
</tr>
</table>

## -remarks

You can also call the 
<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-geterrordescription">IBackgroundCopyManager::GetErrorDescription</a> method to retrieve the error text associated with an error code.

Descriptions for HTTP errors are  localized.

<b>Windows XP/2000:  </b>Descriptions for HTTP errors are not localized.


#### Examples

See the example code in the 
<a href="/windows/desktop/Bits/handling-errors">Handling Errors</a> topic.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyerror-geterror">IBackgroundCopyError::GetError</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyerror-geterrorcontextdescription">IBackgroundCopyError::GetErrorContextDescription</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopyerror-getfile">IBackgroundCopyError::GetFile</a>



<a href="/windows/desktop/api/bits/nf-bits-ibackgroundcopymanager-geterrordescription">IBackgroundCopyManager::GetErrorDescription</a>