---
UID: NF:winnls.NormalizeString
title: NormalizeString function
author: windows-sdk-content
description: Normalizes characters of a text string according to Unicode 4.0 TR#15. For more information, see Using Unicode Normalization to Represent Strings.
old-location: intl\normalizestring.htm
old-project: Intl
ms.assetid: ef76d0e5-2999-4a21-8522-c698013e3816
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: NormalizeString, NormalizeString function [Internationalization for Windows Applications], _win32_NormalizeString, intl.normalizestring, winnls/NormalizeString
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
 - NormalizeString
product: Windows
targetos: Windows
req.lib: 
req.dll: Normaliz.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# NormalizeString function


## -description


Normalizes characters of a text string according to Unicode 4.0 TR#15. For more information, see <a href="https://msdn.microsoft.com/027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35">Using Unicode Normalization to Represent Strings</a>.


## -parameters




### -param NormForm [in]

Normalization form to use. <a href="https://msdn.microsoft.com/d0133c6d-3534-4616-8b6f-07ec712808a3">NORM_FORM</a> specifies the standard Unicode normalization forms.


### -param lpSrcString [in]

Pointer to the non-normalized source string.


### -param cwSrcLength [in]

Length, in characters, of the buffer containing the source string. The application can set this parameter to -1 if the function should assume the string to be null-terminated and calculate the length automatically.


### -param lpDstString [out, optional]

Pointer to a buffer in which the function retrieves the destination string. Alternatively, this parameter contains <b>NULL</b> if <i>cwDstLength</i> is set to 0.

<div class="alert"><b>Note</b>  The function does not null-terminate the string if the input string length is explicitly specified without a terminating null character. To null-terminate the output string, the application should specify -1 or explicitly count the terminating null character for the input string.</div>
<div> </div>

### -param cwDstLength [in]

Length, in characters, of the buffer containing the destination string. Alternatively, the application can set this parameter to 0 to request the function to return the required size for the destination buffer.


## -returns



Returns the length of the normalized string in the destination buffer. If <i>cwDstLength</i> is set to 0, the function returns the estimated buffer length required to do the actual conversion.

If the string in the input buffer is null-terminated or if <i>cwSrcLength</i> is -1, the string written to the destination buffer is null-terminated and the returned string length includes the terminating null character.

The function returns a value that is less than or equal to 0 if it does not succeed. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INSUFFICIENT_BUFFER. A supplied buffer size was not large enough, or it was incorrectly set to <b>NULL</b>.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
<li>ERROR_NO_UNICODE_TRANSLATION. Invalid Unicode was found in a string. The return value is the negative of the index of the location of the error in the input string.</li>
<li>ERROR_SUCCESS. The action completed successfully but yielded no results.</li>
</ul>



## -remarks



Some Unicode characters have multiple equivalent binary representations consisting of sets of combining and/or composite Unicode characters. The Unicode standard defines a process called normalization that returns one binary representation when given any of the equivalent binary representations of a character. Normalization can be performed with several algorithms, called normalization forms, that obey different rules, as described in <a href="https://msdn.microsoft.com/027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35">Using Unicode Normalization to Represent Strings</a>. The Win32 and the .NET Framework currently support normalization forms C, D, KC, and KD, as defined in <a href="http://go.microsoft.com/fwlink/p/?linkid=161647">Unicode Standard Annex #15: Unicode Normalization Forms</a>. Normalized strings are typically evaluated with an ordinal comparison.

The following code demonstrates the use of the buffer length estimate:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>const int maxIterations = 10;
LPWSTR strResult = NULL;
HANDLE hHeap = GetProcessHeap();

int iSizeEstimated = NormalizeString(form, strInput, -1, NULL, 0);
for (int i = 0; i &lt; maxIterations; i++)
{
    if (strResult)
        HeapFree(hHeap, 0, strResult);
    strResult = (LPWSTR)HeapAlloc(hHeap, 0, iSizeEstimated * sizeof (WCHAR));
    iSizeEstimated = NormalizeString(form, strInput, -1, strResult, iSizeEstimated);
 
    if (iSizeEstimated &gt; 0)
        break; // success 
 
    if (iSizeEstimated &lt;= 0)
    {
        DWORD dwError = GetLastError();
        if (dwError != ERROR_INSUFFICIENT_BUFFER) break; // Real error, not buffer error 
 
        // New guess is negative of the return value. 
        iSizeEstimated = -iSizeEstimated;
    }
}
</pre>
</td>
</tr>
</table></span></div>
<b>Windows XP, Windows Server 2003</b>: The required header file and DLL are part of the <a href="http://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en"> "Microsoft Internationalized Domain Name (IDN) Mitigation APIs"</a> download, available at the <a href="http://go.microsoft.com/fwlink/p/?linkid=362">MSDN Download Center</a>.


#### Examples

An example showing the use of this function can be found in <a href="https://msdn.microsoft.com/f1f789f9-f12b-465c-8c84-33a8efa6fbc5">NLS: Unicode Normalization Sample</a>.



<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/5a1d3977-9fe9-457f-b0a2-46b32bcc27db">IsNormalizedString</a>



<a href="https://msdn.microsoft.com/d0133c6d-3534-4616-8b6f-07ec712808a3">NORM_FORM</a>



<a href="https://msdn.microsoft.com/7a548074-0782-45e1-8051-80c3b9d81885">National Language Support</a>



<a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support Functions</a>



<a href="https://msdn.microsoft.com/027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35">Using Unicode Normalization to Represent Strings</a>
 

 

