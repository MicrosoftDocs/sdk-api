---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# ScriptApplyDigitSubstitution function


## -description


Applies the specified digit substitution settings to the specified script control and script state structures.


## -parameters




### -param psds [in]

Pointer to a <a href="https://msdn.microsoft.com/e96bf8b4-7456-4e16-a623-48320104dd66">SCRIPT_DIGITSUBSTITUTE</a> structure. The application sets this parameter to <b>NULL</b> if the function is to call <a href="https://msdn.microsoft.com/2c8c33d5-5cd6-4734-bf44-af7d4b578672">ScriptRecordDigitSubstitution</a> with LOCALE_USER_DEFAULT.


### -param psc [out]

Pointer to a <a href="https://msdn.microsoft.com/4623f606-f67e-48ad-8c1d-d27da5ba556c">SCRIPT_CONTROL</a> structure with the <b>fContextDigits</b> and <b>uDefaultLanguage</b> members updated.


### -param pss [out]

Pointer to a <a href="https://msdn.microsoft.com/4b1724f7-7773-42c0-9c19-fbded5aef14e">SCRIPT_STATE</a> structure with the <b>fDigitSubstitute</b> member updated.


## -returns



Returns S_OK if successful. The function returns a nonzero HRESULT value if it does not succeed.

The function returns E_INVALIDARG if it does not recognize the <b>DigitSubstitute</b> member of <a href="https://msdn.microsoft.com/e96bf8b4-7456-4e16-a623-48320104dd66">SCRIPT_DIGITSUBSTITUTE</a>.




## -remarks



This function does not actually substitute digits. It just fills in the structures that describe the digit substitution policy. See <a href="https://msdn.microsoft.com/e1adc567-0445-4deb-8634-25653f82127c">Displaying Text with Uniscribe</a> for a discussion of the context in which this function is normally called.

<div class="alert"><b>Important</b>  Starting with Windows 8: To maintain the ability to run on Windows 7, a module that uses Uniscribe must specify Usp10.lib before gdi32.lib in its library list.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/6b5267d8-b102-410c-bdc9-831555ca2f84">Digit Shapes</a>



<a href="https://msdn.microsoft.com/e1adc567-0445-4deb-8634-25653f82127c">Displaying Text with Uniscribe</a>



<a href="https://msdn.microsoft.com/4623f606-f67e-48ad-8c1d-d27da5ba556c">SCRIPT_CONTROL</a>



<a href="https://msdn.microsoft.com/e96bf8b4-7456-4e16-a623-48320104dd66">SCRIPT_DIGITSUBSTITUTE</a>



<a href="https://msdn.microsoft.com/4b1724f7-7773-42c0-9c19-fbded5aef14e">SCRIPT_STATE</a>



<a href="https://msdn.microsoft.com/2c8c33d5-5cd6-4734-bf44-af7d4b578672">ScriptRecordDigitSubstitution</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/876e36f5-a91c-490b-87bd-b7cb4993f8c4">Uniscribe Functions</a>
 

 

