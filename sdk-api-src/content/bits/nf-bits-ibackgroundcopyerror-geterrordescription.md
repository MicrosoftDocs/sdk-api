---
UID: NF:bits.IBackgroundCopyError.GetErrorDescription
title: IBackgroundCopyError::GetErrorDescription
author: windows-driver-content
description: Retrieves the error text associated with the error.
old-location: bits\ibackgroundcopyerror_geterrordescription.htm
old-project: Bits
ms.assetid: 57323f38-c2e6-4e40-b357-7df758899f97
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: GetErrorDescription, GetErrorDescription method [BITS], GetErrorDescription method [BITS],IBackgroundCopyError interface, IBackgroundCopyError interface [BITS],GetErrorDescription method, IBackgroundCopyError.GetErrorDescription, IBackgroundCopyError::GetErrorDescription, _drz_ibackgroundcopyerror_geterrordescription, bits.ibackgroundcopyerror_geterrordescription, bits/IBackgroundCopyError::GetErrorDescription
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
req.typenames: BG_JOB_PROXY_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	QmgrPrxy.dll
api_name:
-	IBackgroundCopyError.GetErrorDescription
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IBackgroundCopyError::GetErrorDescription


## -description


Retrieves the error text associated with the error.


## -parameters




### -param LanguageId [in]

Identifies the locale to use to generate the description. To create the language identifier, use the 
<a href="http://go.microsoft.com/fwlink/p/?linkid=166156">MAKELANGID</a> macro. For example, to specify U.S. English, use the following code sample. 




<code>MAKELANGID(LANG_ENGLISH, SUBLANG_ENGLISH_US)</code>

To retrieve the system's default user language identifier, use the following calls.

<code>LANGIDFROMLCID(GetThreadLocale())</code>


### -param pErrorDescription






#### - ppErrorDescription [out]

Null-terminated string that contains the error text associated with the error. Call the 
<a href="http://go.microsoft.com/fwlink/p/?linkid=154376">CoTaskMemFree</a> function to free <i>ppErrorDescription</i> when done.


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
<a href="https://msdn.microsoft.com/e62e2bde-485d-42d4-b824-a682ab9e16ca">IBackgroundCopyManager::GetErrorDescription</a> method to retrieve the error text associated with an error code.

Descriptions for HTTP errors are  localized.

<b>Windows XP/2000:  </b>Descriptions for HTTP errors are not localized.


#### Examples

See the example code in the 
<a href="https://msdn.microsoft.com/cbc182ce-c853-492e-8953-21c54500875b">Handling Errors</a> topic.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/abdf115d-3ff2-4664-b053-f55872ad24ab">IBackgroundCopyError::GetError</a>



<a href="https://msdn.microsoft.com/87f5ae62-c171-4637-bebb-3a5c5aa546b3">IBackgroundCopyError::GetErrorContextDescription</a>



<a href="https://msdn.microsoft.com/7b6d4bd4-2102-4e6b-b250-1d73fae94cf9">IBackgroundCopyError::GetFile</a>



<a href="https://msdn.microsoft.com/e62e2bde-485d-42d4-b824-a682ab9e16ca">IBackgroundCopyManager::GetErrorDescription</a>
 

 

