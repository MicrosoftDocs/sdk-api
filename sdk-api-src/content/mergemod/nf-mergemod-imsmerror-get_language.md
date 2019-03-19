---
UID: NF:mergemod.IMsmError.get_Language
title: IMsmError::get_Language (mergemod.h)
author: windows-sdk-content
description: The get_Language method retrieves the Language property of the Error object. This function returns the LANGID of the error.
old-location: setup\imsmerror_get_language.htm
tech.root: Msi
ms.assetid: c0d14c18-facc-441c-89c6-85abe6d19443
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMsmError interface,get_Language method, IMsmError.get_Language, IMsmError::get_Language, _msi_get_language_function_error_object_, get_Language, get_Language method, get_Language method,IMsmError interface, mergemod/IMsmError::get_Language, setup.imsmerror_get_language
ms.topic: method
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mergemod.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmError.get_Language
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMsmError::get_Language


## -description


The 
<b>get_Language</b> method retrieves the 
<a href="https://msdn.microsoft.com/9b0608d1-b6e8-4cf9-8119-3c2909156516">Language</a> property of the 
<a href="https://msdn.microsoft.com/38025e21-2d31-40f8-a088-2d3912c2893e">Error</a> object. This function returns the <b>LANGID</b> of the error.


## -parameters




### -param ErrorLanguage [out]

A pointer to a location in memory that receives the language value causing this error.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Language is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -remarks



The function returns -1 unless the error is of type msmErrorLanguageUnsupported or msmErrorLanguageFailed. You can determine the type of error by calling <a href="https://msdn.microsoft.com/733a5390-419d-414a-b50e-8400d179bfb6">IMsmError::get_Type</a>.




## -see-also




<a href="https://msdn.microsoft.com/877d3691-948f-4aea-89d8-0ff008126ccc">Merge Module Automation</a>
 

 

