---
UID: NF:winbase.FormatMessageA
title: FormatMessageA function (winbase.h)
description: Formats a message string. (FormatMessageA)
helpviewer_keywords: ["FORMAT_MESSAGE_ALLOCATE_BUFFER", "FORMAT_MESSAGE_ARGUMENT_ARRAY", "FORMAT_MESSAGE_FROM_HMODULE", "FORMAT_MESSAGE_FROM_STRING", "FORMAT_MESSAGE_FROM_SYSTEM", "FORMAT_MESSAGE_IGNORE_INSERTS", "FORMAT_MESSAGE_MAX_WIDTH_MASK", "FormatMessageA", "winbase/FormatMessageA"]
old-location: base\formatmessage.htm
tech.root: Debug
ms.assetid: b9d61342-4bcf-42e9-96f1-a5993dfb6c0c
ms.date: 12/05/2018
ms.keywords: FORMAT_MESSAGE_ALLOCATE_BUFFER, FORMAT_MESSAGE_ARGUMENT_ARRAY, FORMAT_MESSAGE_FROM_HMODULE, FORMAT_MESSAGE_FROM_STRING, FORMAT_MESSAGE_FROM_SYSTEM, FORMAT_MESSAGE_IGNORE_INSERTS, FORMAT_MESSAGE_MAX_WIDTH_MASK, FormatMessage, FormatMessage function, FormatMessageA, FormatMessageW, _win32_formatmessage, base.formatmessage, winbase/FormatMessage, winbase/FormatMessageA, winbase/FormatMessageW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FormatMessageW (Unicode) and FormatMessageA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FormatMessageA
 - winbase/FormatMessageA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-localization-l1-2-4.dll
 - api-ms-win-core-localization-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-Core-misc-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - FormatMessage
 - FormatMessageA
 - FormatMessageW
---

# FormatMessageA function


## -description

Formats a message string. The function requires a message definition as input. The message 
    definition can come from a buffer passed into the function. It can come from a message table resource in an 
    already-loaded module. Or the caller can ask the function to search the system's message table resource(s) for the 
    message definition. The function finds the message definition in a message table resource based on a message 
    identifier and a language identifier. The function copies the formatted message text to an output buffer, 
    processing any embedded insert sequences if requested.

## -parameters

### -param dwFlags [in]

The formatting options, and how to interpret the <i>lpSource</i> parameter. The 
       low-order byte of <i>dwFlags</i> specifies how the function handles line breaks in the output 
       buffer. The low-order byte can also specify the maximum width of a formatted output line.

This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FORMAT_MESSAGE_ALLOCATE_BUFFER"></a><a id="format_message_allocate_buffer"></a><dl>
<dt><b>FORMAT_MESSAGE_ALLOCATE_BUFFER</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
The function allocates a buffer large enough to hold the formatted message, and places a pointer to the 
         allocated buffer at the address specified by <i>lpBuffer</i>. The 
         <i>lpBuffer</i> parameter is a pointer to an <b>LPTSTR</b>; you must 
         cast the pointer to an <b>LPTSTR</b> (for example, 
         <code>(LPTSTR)&amp;lpBuffer</code>). The <i>nSize</i> 
         parameter specifies the minimum number of <b>TCHARs</b> to allocate for an output 
         message buffer. The caller should use the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> 
         function to free the buffer when it is no longer needed.

If the length of the formatted message exceeds 128K bytes, then 
         <b>FormatMessage</b> will fail and a subsequent call to 
         <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return 
         <b>ERROR_MORE_DATA</b>.

In previous versions of Windows, this value was not available for use when compiling Windows Store apps. As of Windows 10 this value can be used. 

<b>Windows Server 2003 and Windows XP:  </b><p class="note">If the length of the formatted message exceeds 128K bytes, then 
           <b>FormatMessage</b> will not automatically fail with an 
           error of <b>ERROR_MORE_DATA</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_MESSAGE_ARGUMENT_ARRAY"></a><a id="format_message_argument_array"></a><dl>
<dt><b>FORMAT_MESSAGE_ARGUMENT_ARRAY</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
The <i>Arguments</i> parameter is not a <b>va_list</b> 
         structure, but is a pointer to an array of values that represent the arguments.

This flag cannot be used with 64-bit integer values.  If you are using a 64-bit integer, you must use the 
         <b>va_list</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_MESSAGE_FROM_HMODULE"></a><a id="format_message_from_hmodule"></a><dl>
<dt><b>FORMAT_MESSAGE_FROM_HMODULE</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
The <i>lpSource</i> parameter is a module handle containing the message-table 
         resource(s) to search. If this <i>lpSource</i> handle is <b>NULL</b>, 
         the current process's application image file will be searched. This flag cannot be used with 
        <b>FORMAT_MESSAGE_FROM_STRING</b>.

If the module has no message table resource, the function fails with 
         <b>ERROR_RESOURCE_TYPE_NOT_FOUND</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_MESSAGE_FROM_STRING"></a><a id="format_message_from_string"></a><dl>
<dt><b>FORMAT_MESSAGE_FROM_STRING</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
The <i>lpSource</i> parameter is a pointer to a null-terminated string that contains 
        a message definition. The message definition may contain insert sequences, just as the message text in a 
        message table resource may. This flag cannot be used with 
        <b>FORMAT_MESSAGE_FROM_HMODULE</b> or 
        <b>FORMAT_MESSAGE_FROM_SYSTEM</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_MESSAGE_FROM_SYSTEM"></a><a id="format_message_from_system"></a><dl>
<dt><b>FORMAT_MESSAGE_FROM_SYSTEM</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
The function should search the system message-table resource(s) for the requested message. If this flag is 
         specified with <b>FORMAT_MESSAGE_FROM_HMODULE</b>, the function searches the system 
         message table if the message is not found in the module specified by <i>lpSource</i>. This 
         flag cannot be used with <b>FORMAT_MESSAGE_FROM_STRING</b>.

If this flag is specified, an application can pass the result of the 
         <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to retrieve the message text 
         for a system-defined error.

</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_MESSAGE_IGNORE_INSERTS"></a><a id="format_message_ignore_inserts"></a><dl>
<dt><b>FORMAT_MESSAGE_IGNORE_INSERTS</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Insert sequences in the message definition such as %1 are to be ignored and passed through to the output buffer 
        unchanged. This flag is useful for fetching a message for later formatting. If this flag is set, the 
        <i>Arguments</i> parameter is ignored.

</td>
</tr>
</table>
 

The low-order byte of <i>dwFlags</i> can specify the maximum width of a formatted output 
       line. The following are possible values of the low-order byte.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
There are no output line width restrictions. The function stores line breaks that are in the message 
        definition text into the output buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_MESSAGE_MAX_WIDTH_MASK"></a><a id="format_message_max_width_mask"></a><dl>
<dt><b>FORMAT_MESSAGE_MAX_WIDTH_MASK</b></dt>
<dt>0x000000FF</dt>
</dl>
</td>
<td width="60%">
The function ignores regular line breaks in the message definition text. The function stores hard-coded 
        line breaks in the message definition text into the output buffer. The function generates no new line 
        breaks.

</td>
</tr>
</table>
 

If the low-order byte is a nonzero value other than 
      <b>FORMAT_MESSAGE_MAX_WIDTH_MASK</b>, it specifies the maximum number of characters in an 
      output line. The function ignores regular line breaks in the message definition text. The function never splits 
      a string delimited by white space across a line break. The function stores hard-coded line breaks in the message 
      definition text into the output buffer. Hard-coded line breaks are coded with the %n escape sequence.

### -param lpSource [in, optional]

The location of the message definition. The type of this parameter depends upon the settings in the 
      <i>dwFlags</i> parameter.

<table>
<tr>
<th><i>dwFlags</i> Setting</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FORMAT_MESSAGE_FROM_HMODULE"></a><a id="format_message_from_hmodule"></a><dl>
<dt><b>FORMAT_MESSAGE_FROM_HMODULE</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
A handle to the module that contains the message table to search.

</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_MESSAGE_FROM_STRING"></a><a id="format_message_from_string"></a><dl>
<dt><b>FORMAT_MESSAGE_FROM_STRING</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
Pointer to a string that consists of unformatted message text. It will be scanned for inserts and 
        formatted accordingly.

</td>
</tr>
</table>
 

If neither of these flags is set in <i>dwFlags</i>, then 
       <i>lpSource</i> is ignored.

### -param dwMessageId [in]

The message identifier for the requested message. This parameter is ignored if 
      <i>dwFlags</i> includes <b>FORMAT_MESSAGE_FROM_STRING</b>.

### -param dwLanguageId [in]

The <a href="/windows/desktop/Intl/language-identifiers">language identifier</a> for the requested 
       message. This parameter is ignored if <i>dwFlags</i> includes 
       <b>FORMAT_MESSAGE_FROM_STRING</b>.

If you pass a specific <b>LANGID</b> in this parameter, 
       <b>FormatMessage</b> will return a message for that 
       <b>LANGID</b> only. If the function cannot find a message for that 
       <b>LANGID</b>, it sets Last-Error to 
       <b>ERROR_RESOURCE_LANG_NOT_FOUND</b>. If you pass in zero, 
       <b>FormatMessage</b> looks for a message for 
       <b>LANGIDs</b> in the following order:

<ol>
<li>Language neutral</li>
<li>Thread <b>LANGID</b>, based on the thread's locale value</li>
<li>User default <b>LANGID</b>, based on the user's default locale value</li>
<li>System default <b>LANGID</b>, based on the system default locale value</li>
<li>US English</li>
</ol>
If <b>FormatMessage</b> does not locate a message for any 
       of the preceding <b>LANGIDs</b>, it returns any language message string that is present. 
       If that fails, it returns <b>ERROR_RESOURCE_LANG_NOT_FOUND</b>.

### -param lpBuffer [out]

A pointer to a buffer that receives the null-terminated string that specifies the formatted message. If 
       <i>dwFlags</i> includes <b>FORMAT_MESSAGE_ALLOCATE_BUFFER</b>, the 
       function allocates a buffer using the <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> 
       function, and places the pointer to the buffer at the address specified in 
       <i>lpBuffer</i>.

This buffer cannot be larger than 64K bytes.

### -param nSize [in]

If the <b>FORMAT_MESSAGE_ALLOCATE_BUFFER</b> flag is not set, this parameter specifies 
       the size of the output buffer, in <b>TCHARs</b>. If 
       <b>FORMAT_MESSAGE_ALLOCATE_BUFFER</b> is set, this parameter specifies the minimum number of 
       <b>TCHARs</b> to allocate for an output buffer.

The output buffer cannot be larger than 64K bytes.

### -param Arguments [in, optional]

An array of values that are used as insert values in the formatted message. A %1 in the format string 
       indicates the first value in the <i>Arguments</i> array; a %2 indicates the second argument; 
       and so on.

The interpretation of each value depends on the formatting information associated with the insert in the 
       message definition. The default is to treat each value as a pointer to a null-terminated string.

By default, the <i>Arguments</i> parameter is of type 
       <b>va_list*</b>, which is a language- and implementation-specific data type for 
       describing a variable number of arguments. The state of the <b>va_list</b> argument is 
       undefined upon return from the function. To use the <b>va_list</b> again, destroy the 
       variable argument list pointer using <b>va_end</b> and reinitialize it with 
       <b>va_start</b>.

If you do not have a pointer of type 
       <b>va_list*</b>, then specify the <b>FORMAT_MESSAGE_ARGUMENT_ARRAY</b> 
       flag and pass a pointer to an array of <b>DWORD_PTR</b> values; those values are input to 
       the message formatted as the insert values. Each insert must have a corresponding element in the array.

## -returns

If the function succeeds, the return value is the number of <b>TCHARs</b> stored in the 
       output buffer, excluding the terminating null character.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Within the message text, several escape sequences are supported for dynamically formatting the message. These 
    escape sequences and their meanings are shown in the following tables. All escape sequences start with the percent 
    character (%).

<table>
<tr>
<th>Escape sequence</th>
<th>Meaning</th>
</tr>
<tr>
<td>%0</td>
<td>Terminates a message text line without a trailing new line character. This escape sequence can be used to 
       build up long lines or to terminate the message itself without a trailing new line character. It is useful for 
       prompt messages.</td>
</tr>
<tr>
<td>%<i>n</i>!<i>format string</i>!</td>
<td>
Identifies an insert sequence. The value of <i>n</i> can be in the range from 1 through 99. The 
        format string (which must be surrounded by exclamation marks) is optional and defaults to !s! if not 
        specified. For more information, see 
        <a href="/cpp/c-runtime-library/format-specification-syntax-printf-and-wprintf-functions">Format Specification Fields</a>.

The format string can include a width and precision specifier for strings and a width specifier for 
        integers. Use an asterisk (*) to specify the width and precision. For example, %1!*.*s! or %1!*u!.

If you do not use the width and precision specifiers, the insert numbers correspond directly to the input 
        arguments. For example, if the source string is "%1 %2 %1" and the input arguments are "Bill" and "Bob", the 
        formatted output string is "Bill Bob Bill".

However, if you use a width and precision specifier, the insert numbers do not correspond directly to the 
        input arguments. For example, the insert numbers for the previous example could change to 
        "%1!*.*s! %4 %5!*s!".

The insert numbers depend on whether you use an arguments array 
        (<b>FORMAT_MESSAGE_ARGUMENT_ARRAY</b>) or a <b>va_list</b>. For an 
        arguments array, the next insert number is <i>n+2</i> if the previous format string 
        contained one asterisk and is <i>n+3</i> if two asterisks were specified. For a 
        <b>va_list</b>, the next insert number is <i>n+1</i> if the previous 
        format string contained one asterisk and is <i>n+2</i> if two asterisks were specified.

If you want to repeat "Bill", as in the previous example, the arguments must include "Bill" twice. For 
        example, if the source string is "%1!*.*s! %4 %5!*s!", the arguments could be, 4, 2, Bill, Bob, 6, Bill 
        (if using the <b>FORMAT_MESSAGE_ARGUMENT_ARRAY</b> flag). The formatted string would then 
        be "  Bi Bob   Bill".

Repeating insert numbers when the source string contains width and precision specifiers may not yield the 
        intended results. If you replaced %5 with %1, the function would try to print a string at address 6 (likely 
        resulting in an access violation).

Floating-point format specifiers—e, E, f, and g—are not supported. 
        The workaround is to use the <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa">StringCchPrintf</a> 
        function to format the floating-point number into a temporary buffer, then use that buffer as the insert 
        string.

Inserts that use the I64 prefix are treated as two 32-bit arguments. They must be used before subsequent 
        arguments are used. Note that it may be easier for you to use 
        <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa">StringCchPrintf</a> instead of this prefix.

</td>
</tr>
</table>
 

Any other nondigit character following a percent character is formatted in the output message without the 
    percent character. Following are some examples.

<table>
<tr>
<th>Format string</th>
<th>Resulting output</th>
</tr>
<tr>
<td>%%</td>
<td>A single percent sign.</td>
</tr>
<tr>
<td>%<i>space</i></td>
<td>A single space. This format string can be used to ensure the appropriate number of trailing spaces in a 
       message text line.</td>
</tr>
<tr>
<td>%.</td>
<td>A single period. This format string can be used to include a single period at the beginning of a line 
       without terminating the message text definition.</td>
</tr>
<tr>
<td>%!</td>
<td>A single exclamation point. This format string can be used to include an exclamation point immediately after 
       an insert without its being mistaken for the beginning of a format string.</td>
</tr>
<tr>
<td>%n</td>
<td>A hard line break when the format string occurs at the end of a line. This format string is 
       useful when <b>FormatMessage</b> is supplying regular line 
       breaks so the message fits in a certain width.</td>
</tr>
<tr>
<td>%r</td>
<td>A hard carriage return without a trailing newline character.</td>
</tr>
<tr>
<td>%t</td>
<td>A single tab.</td>
</tr>
</table>
 

<h3><a id="Security_Remarks"></a><a id="security_remarks"></a><a id="SECURITY_REMARKS"></a>Security Remarks</h3>
If this function is called without <b>FORMAT_MESSAGE_IGNORE_INSERTS</b>, the 
      <i>Arguments</i> parameter must contain enough parameters to satisfy all insertion sequences 
      in the message string, and they must be of the correct type. Therefore, do not use untrusted or unknown message 
      strings with inserts enabled because they can contain more insertion sequences than 
      <i>Arguments</i> provides, or those that may be of the wrong type. In particular, it is 
      unsafe to take an arbitrary system error code returned from an API and use 
      <b>FORMAT_MESSAGE_FROM_SYSTEM</b> without 
      <b>FORMAT_MESSAGE_IGNORE_INSERTS</b>.


#### Examples

The <b>FormatMessage</b> function can be used to obtain 
     error message strings for the system error codes returned by 
     <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. For an example, see 
     <a href="/windows/desktop/Debug/retrieving-the-last-error-code">Retrieving the Last-Error Code</a>.

<div class="code"></div>
The following example shows how to use an argument array and the width and precision specifiers.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <stdio.h>

void main(void)
{
    LPWSTR pMessage = L"%1!*.*s! %4 %5!*s!";
    DWORD_PTR pArgs[] = { (DWORD_PTR)4, (DWORD_PTR)2, (DWORD_PTR)L"Bill",  // %1!*.*s! refers back to the first insertion string in pMessage
         (DWORD_PTR)L"Bob",                                                // %4 refers back to the second insertion string in pMessage
         (DWORD_PTR)6, (DWORD_PTR)L"Bill" };                               // %5!*s! refers back to the third insertion string in pMessage
    const DWORD size = 100+1;
    WCHAR buffer[size];


    if (!FormatMessage(FORMAT_MESSAGE_FROM_STRING | FORMAT_MESSAGE_ARGUMENT_ARRAY,
                       pMessage, 
                       0,
                       0,
                       buffer, 
                       size, 
                       (va_list*)pArgs))
    {
        wprintf(L"Format message failed with 0x%x\n", GetLastError());
        return;
    }

    // Buffer contains "  Bi Bob   Bill".
    wprintf(L"Formatted message: %s\n", buffer);
}


```


The following example shows how to implement the previous example using 
     <b>va_list</b>.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <stdio.h>

LPWSTR GetFormattedMessage(LPWSTR pMessage, ...);

void main(void)
{
    LPWSTR pBuffer = NULL;
    LPWSTR pMessage = L"%1!*.*s! %3 %4!*s!";

    // The variable length arguments correspond directly to the format
    // strings in pMessage.
    pBuffer = GetFormattedMessage(pMessage, 4, 2, L"Bill", L"Bob", 6, L"Bill");
    if (pBuffer)
    {
        // Buffer contains "  Bi Bob   Bill".
        wprintf(L"Formatted message: %s\n", pBuffer);
        LocalFree(pBuffer);
    }
    else
    {
        wprintf(L"Format message failed with 0x%x\n", GetLastError());
    }
}

// Formats a message string using the specified message and variable
// list of arguments.
LPWSTR GetFormattedMessage(LPWSTR pMessage, ...)
{
    LPWSTR pBuffer = NULL;

    va_list args = NULL;
    va_start(args, pMessage);

    FormatMessage(FORMAT_MESSAGE_FROM_STRING |
                  FORMAT_MESSAGE_ALLOCATE_BUFFER,
                  pMessage, 
                  0,
                  0,
                  (LPWSTR)&pBuffer, 
                  0, 
                  &args);

    va_end(args);

    return pBuffer;
}

```






> [!NOTE]
> The winbase.h header defines FormatMessage as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/error-handling-functions">Error Handling Functions</a>



<a href="/windows/desktop/WES/message-compiler--mc-exe-">Message Compiler</a>



Message Tables
