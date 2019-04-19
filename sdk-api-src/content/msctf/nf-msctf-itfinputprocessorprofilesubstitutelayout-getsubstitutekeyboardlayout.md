---
UID: NF:msctf.ITfInputProcessorProfileSubstituteLayout.GetSubstituteKeyboardLayout
title: ITfInputProcessorProfileSubstituteLayout::GetSubstituteKeyboardLayout (msctf.h)
author: windows-sdk-content
description: ITfInputProcessorProfileSubstituteLayout::GetSubstituteKeyboardLayout method
old-location: tsf\getsubstitutekeyboardlayout.htm
tech.root: TSF
ms.assetid: 9006a76f-11db-4e8c-9133-c335af7fe5ff
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSubstituteKeyboardLayout, GetSubstituteKeyboardLayout method [Text Services Framework], GetSubstituteKeyboardLayout method [Text Services Framework],ITfInputProcessorProfileSubstituteLayout interface, ITfInputProcessorProfileSubstituteLayout interface [Text Services Framework],GetSubstituteKeyboardLayout method, ITfInputProcessorProfileSubstituteLayout.GetSubstituteKeyboardLayout, ITfInputProcessorProfileSubstituteLayout::GetSubstituteKeyboardLayout, textstor/ITfInputProcessorProfileSubstituteLayout::GetSubstituteKeyboardLayout, tsf.getsubstitutekeyboardlayout
ms.topic: method
req.header: msctf.h
req.include-header: Msctf.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfInputProcessorProfileSubstituteLayout.GetSubstituteKeyboardLayout
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfInputProcessorProfileSubstituteLayout::GetSubstituteKeyboardLayout


## -description




## -parameters




### -param rclsid [in]

Contains the class identifier of the text service.


### -param langid [in]

Specifies the language of the profile. See <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">Language Identifiers</a>.


### -param guidProfile [in]

Identifies the profile GUID.


### -param phKL [out]

Pointer to an <b>HKL</b> value that specifies the substitute input locale identifier.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e801ca27-4581-4369-886c-04b824d55013">ITfInputProcessorProfileSubstituteLayout</a>



<a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">Language Identifiers</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646305(v=VS.85).aspx">LoadKeyboardLayout</a>



<a href="https://msdn.microsoft.com/95676067-ab5c-470b-a4be-117ab6810d48">Text Service Registration</a>
 

 

