---
UID: NF:winnls.IsNormalizedString
title: IsNormalizedString function
author: windows-sdk-content
description: Verifies that a string is normalized according to Unicode 4.0 TR#15. For more information, see Using Unicode Normalization to Represent Strings.
old-location: intl\isnormalizedstring.htm
old-project: Intl
ms.assetid: 5a1d3977-9fe9-457f-b0a2-46b32bcc27db
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IsNormalizedString, IsNormalizedString function [Internationalization for Windows Applications], _win32_IsNormalizedString, intl.isnormalizedstring, winnls/IsNormalizedString
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NORM_FORM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Normaliz.dll
 - API-MS-Win-Core-normalization-l1-1-0.dll
 - KernelBase.dll
api_name:
 - IsNormalizedString
product: Windows
targetos: Windows
req.lib: 
req.dll: Normaliz.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IsNormalizedString function


## -description


Verifies that a string is normalized according to Unicode 4.0 TR#15. For more information, see <a href="https://msdn.microsoft.com/027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35">Using Unicode Normalization to Represent Strings</a>.


## -parameters




### -param NormForm [in]

Normalization form to use. <a href="https://msdn.microsoft.com/d0133c6d-3534-4616-8b6f-07ec712808a3">NORM_FORM</a> specifies the standard Unicode normalization forms.


### -param lpString [in]

Pointer to the string to test.


### -param cwLength [in]

Length, in characters, of the input string, including a null terminating character. If this value is -1, the function assumes the string to be null-terminated and calculates the length automatically.


## -returns



Returns <b>TRUE</b> if the input string is already normalized to the appropriate form, or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
<li>ERROR_NO_UNICODE_TRANSLATION. Invalid Unicode was found in string.</li>
<li>ERROR_SUCCESS. The action completed successfully but yielded no results.</li>
</ul>
If you need to reliably determine <b>FALSE</b> from an error condition, then it must call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a>(ERROR_SUCCESS). 
          




## -remarks



<b>Windows XP, Windows Server 2003</b>: The required header file and DLL are part of the <a href="http://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en"> "Microsoft Internationalized Domain Name (IDN) Mitigation APIs"</a> download, available at the <a href="http://go.microsoft.com/fwlink/p/?linkid=362">MSDN Download Center</a>.


#### Examples

An example showing the use of this function can be found in <a href="https://msdn.microsoft.com/f1f789f9-f12b-465c-8c84-33a8efa6fbc5">NLS: Unicode Normalization Sample</a>.



<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d0133c6d-3534-4616-8b6f-07ec712808a3">NORM_FORM</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/ef76d0e5-2999-4a21-8522-c698013e3816">NormalizeString</a>



<a href="https://msdn.microsoft.com/027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35">Using Unicode Normalization to Represent Strings</a>
 

 

