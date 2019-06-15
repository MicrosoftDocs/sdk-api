---
UID: NF:msctf.ITfInputProcessorProfiles.SubstituteKeyboardLayout
title: ITfInputProcessorProfiles::SubstituteKeyboardLayout (msctf.h)
author: windows-sdk-content
description: ITfInputProcessorProfiles::SubstituteKeyboardLayout method
old-location: tsf\itfinputprocessorprofiles_substitutekeyboardlayout.htm
tech.root: TSF
ms.assetid: e069f515-d5f6-4acd-a3ff-0c3c60c785ac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfInputProcessorProfiles interface [Text Services Framework],SubstituteKeyboardLayout method, ITfInputProcessorProfiles.SubstituteKeyboardLayout, ITfInputProcessorProfiles::SubstituteKeyboardLayout, SubstituteKeyboardLayout, SubstituteKeyboardLayout method [Text Services Framework], SubstituteKeyboardLayout method [Text Services Framework],ITfInputProcessorProfiles interface, _tsf_itfinputprocessorprofiles_substitutekeyboardlayout_ref, msctf/ITfInputProcessorProfiles::SubstituteKeyboardLayout, tsf.itfinputprocessorprofiles_substitutekeyboardlayout
ms.topic: method
f1_keywords: ["msctf/ITfInputProcessorProfiles.SubstituteKeyboardLayout"]
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
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
 - Msctf.dll
api_name:
 - ITfInputProcessorProfiles.SubstituteKeyboardLayout
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfInputProcessorProfiles::SubstituteKeyboardLayout


## -description




## -parameters




### -param rclsid [in]

Contains the CLSID of the text service of the profile in question.


### -param langid [in]

Contains a <b>LANGID</b> value that specifies the language of the profile in question.


### -param guidProfile [in]

Contains a GUID value that identifies the profile in question.


### -param hKL [in]

Contains an <b>HKL</b> value that specifies the input locale identifier for the substitute keyboard. Obtain this value by calling <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-loadkeyboardlayouta">LoadKeyboardLayout</a>.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-loadkeyboardlayouta">LoadKeyboardLayout</a>
 

 

