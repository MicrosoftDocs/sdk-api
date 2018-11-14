---
UID: NF:bits.IBackgroundCopyError.GetErrorContextDescription
title: IBackgroundCopyError::GetErrorContextDescription
author: windows-sdk-content
description: Retrieves the description of the context in which the error occurred.
old-location: bits\ibackgroundcopyerror_geterrorcontextdescription.htm
tech.root: Bits
ms.assetid: 87f5ae62-c171-4637-bebb-3a5c5aa546b3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetErrorContextDescription, GetErrorContextDescription method [BITS], GetErrorContextDescription method [BITS],IBackgroundCopyError interface, IBackgroundCopyError interface [BITS],GetErrorContextDescription method, IBackgroundCopyError.GetErrorContextDescription, IBackgroundCopyError::GetErrorContextDescription, _drz_ibackgroundcopyerror_geterrorcontextdescription, bits.ibackgroundcopyerror_geterrorcontextdescription, bits/IBackgroundCopyError::GetErrorContextDescription
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyError.GetErrorContextDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- bits.h
: 
- IBackgroundCopyError.GetErrorContextDescription
: 
---

# IBackgroundCopyError::GetErrorContextDescription


## -description


Retrieves the description of the context in which the error occurred.


## -parameters




### -param LanguageId [in]

Identifies the locale to use to generate the description. To create the language identifier, use the 
<a href="http://go.microsoft.com/fwlink/p/?linkid=166156">MAKELANGID</a> macro. For example, to specify U.S. English, use the following code sample. 




<code>MAKELANGID(LANG_ENGLISH, SUBLANG_ENGLISH_US)</code>

To retrieve the system's default user language identifier, use the following calls.

<code>LANGIDFROMLCID(GetThreadLocale())</code>


### -param pContextDescription

TBD




#### - ppContextDescription [out]

Null-terminated string that contains the description of the context in which the error occurred. Call the 
<a href="http://go.microsoft.com/fwlink/p/?linkid=154376">CoTaskMemFree</a> function to free <i>ppContextDescription</i> when done.


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Description of the context was successfully retrieved.

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
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362876(v=VS.85).aspx">IBackgroundCopyError::GetError</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362878(v=VS.85).aspx">IBackgroundCopyError::GetErrorDescription</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362879(v=VS.85).aspx">IBackgroundCopyError::GetFile</a>
 

 

