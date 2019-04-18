---
UID: NL:chstring.CHString
title: CHString (chstring.h)
author: windows-sdk-content
description: The following table lists the CHString methods.
old-location: wmi\chstring.htm
tech.root: WmiSdk
ms.assetid: e2e4378f-d842-4bca-bffc-a60e718caed3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "??1CHString@@QAE@XZ, ??1CHString@@QEAA@XZ, CHString, CHString class [Windows Management Instrumentation], CHString class [Windows Management Instrumentation],described, _hmm_chstring, chstring/CHString, wmi.chstring"
ms.topic: class
req.header: chstring.h
req.include-header: FwCommon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHString
 - ??1CHString@@QAE@XZ
 - ??1CHString@@QEAA@XZ
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CHString class


## -description


<p class="CCE_Message">[The <b>CHString</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The following table lists the <b>CHString</b> methods.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">CHString</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Operators</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">CHString</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d49e1600-d5d4-4c44-81c5-1b8c53b768de">CHString</a>
</td>
<td align="left" width="63%">
Constructs <b>CHString</b> strings in various ways.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>CHString</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21eb9990-a07f-4d6c-b674-dc35f395e603">AllocSysString</a>
</td>
<td align="left" width="63%">
Allocates a BSTR from <b>CHString</b> data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6c88b83-a369-4cb2-9297-df9c5911d08f">Collate</a>
</td>
<td align="left" width="63%">
Compares two strings (case sensitive; uses locale-specific information).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e587dd3-b3ae-4afa-9582-b3867d2fb7ef">Compare</a>
</td>
<td align="left" width="63%">
Compares two strings (case sensitive).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72ad2532-ece8-43e2-b768-7dec6a378c98">CompareNoCase</a>
</td>
<td align="left" width="63%">
Compares two strings (case insensitive).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/837344de-d8dd-45a8-8d43-09d926f51ff9">Empty</a>
</td>
<td align="left" width="63%">
Forces a string to have 0 (zero) length.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98a7c5ad-5bc7-4918-b978-45d2b439f250">Find</a>
</td>
<td align="left" width="63%">Overloaded. Finds a character or substring inside a larger string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3f9111d-9191-4ba5-877a-736e11d0a168">FindOneOf</a>
</td>
<td align="left" width="63%">
Finds the first matching character from a set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95d24b0e-3580-4a5d-8dad-50d44ef1ca39">Format</a>
</td>
<td align="left" width="63%">Overloaded. Formats the string as <b>sprintf</b> does.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45780467-d3aa-4927-aa53-60e5ee277c27">FormatMessageW</a>
</td>
<td align="left" width="63%">Overloaded. Formats a message string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55488cf0-0098-4d5b-b451-a5d56f30ed65">FormatV</a>
</td>
<td align="left" width="63%">
Formats the string as <b>vsprintf</b> does.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4330564e-aeae-4ff3-b01d-eceace721c14">FreeExtra</a>
</td>
<td align="left" width="63%">
Removes any overhead of this string by freeing any extra memory previously allocated to the string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6761c83-d5f2-4900-9863-96692fe897fa">GetAllocLength</a>
</td>
<td align="left" width="63%">
Returns the size of the string buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed038b41-211c-4483-99cd-0bc43b241761">GetAt</a>
</td>
<td align="left" width="63%">Overloaded. Returns the character at a given position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07fa7cae-8af6-491b-a561-8947afde47ab">GetBuffer</a>
</td>
<td align="left" width="63%">
Returns a pointer to the characters in the <b>CHString</b> string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de40f3a3-1880-426d-b3c2-864f0f45f218">GetBufferSetLength</a>
</td>
<td align="left" width="63%">
Returns a pointer to the characters in the <b>CHString</b> string, truncating to the specified length.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb463c0d-8cb3-40b8-9c81-ce98c859068a">GetData</a>
</td>
<td align="left" width="63%">
Returns a pointer to the data in the <b>CHString</b> string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b898f9d1-b9a2-4c7b-a7c0-1b6b51ae565f">GetLength</a>
</td>
<td align="left" width="63%">
Returns the number of Unicode characters in a <b>CHString</b> string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06af1063-1e5a-4a09-a0d7-b5567b9efcff">IsEmpty</a>
</td>
<td align="left" width="63%">
Tests whether a <b>CHString</b> string contains no characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52219bbb-0a88-47b3-ac6c-ba54d15e8157">Left</a>
</td>
<td align="left" width="63%">
Extracts the left part of a string (like the Basic <b>LEFT$</b> function).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5dca7ce-41b2-4290-bb15-23e0a8d64bd1">LoadStringW</a>
</td>
<td align="left" width="63%">
Loads an existing <b>CHString</b> string from a resource file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/820a3ff5-4f99-40b0-8a9d-e5c22fea7ddb">LockBuffer</a>
</td>
<td align="left" width="63%">
Disables reference counting and protects the string in the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5031bbd0-d7a6-4b58-b338-da875c24ad25">MakeLower</a>
</td>
<td align="left" width="63%">
Converts all of the characters in this string to lowercase characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/129792cf-e442-4491-b921-273363809210">MakeReverse</a>
</td>
<td align="left" width="63%">
Reverses the characters in this string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7dbce906-9eb3-47d6-9076-20e092b6239e">MakeUpper</a>
</td>
<td align="left" width="63%">
Converts all of the characters in this string to uppercase characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2036813b-f991-4ca3-95d3-8bbe858aae09">Mid</a>
</td>
<td align="left" width="63%">Overloaded. Extracts the middle part of a string (like the Basic <b>MID$</b> function).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55de2960-8a71-48cc-862b-7cf9a4edf8ea">ReleaseBuffer</a>
</td>
<td align="left" width="63%">
Releases control of the buffer returned by <a href="https://msdn.microsoft.com/07fa7cae-8af6-491b-a561-8947afde47ab">GetBuffer</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/941c9eb3-a5b8-42b7-bb9f-732eaf1faa24">ReverseFind</a>
</td>
<td align="left" width="63%">
Finds a character inside a larger string; starts from the end.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eccf928f-75ac-4442-90f9-0e0578c5798f">Right</a>
</td>
<td align="left" width="63%">
Extracts the right part of a string (like the Basic <b>RIGHT$</b> function).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccac0f07-a272-41b0-950c-7e5d97d9f1d7">SetAt</a>
</td>
<td align="left" width="63%">
Sets a character at a given position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ddadf16-0177-4f96-a5ca-e1b8891473e6">SpanExcluding</a>
</td>
<td align="left" width="63%">
Extracts a substring that contains only the characters that are not in the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d99ce931-c6ec-4f1c-b4ab-144dc930f990">SpanIncluding</a>
</td>
<td align="left" width="63%">
Extracts a substring that contains only the characters in a set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f64181b-eae9-4c65-8fa5-d9171a1e2de8">TrimLeft</a>
</td>
<td align="left" width="63%">
Trims leading whitespace characters from the string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e87ad3c4-d27a-403c-b59e-391d8021e87b">TrimRight</a>
</td>
<td align="left" width="63%">
Trims trailing whitespace characters from the string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cde732ea-b2de-4eb7-bef6-bed01137d76a">UnlockBuffer</a>
</td>
<td align="left" width="63%">
Enables reference counting and releases the string in the buffer.

</td>
</tr>
</table> 
<h3><a id="operators"></a>Operators</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">CHString</b> class has these operators.
<table>
<tr>
<th align="left" width="37%">Operator</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ab84140-31c8-4759-aaee-f79408e7d61c">operator != (CHString, CHString)</a>
</td>
<td align="left" width="63%">
Compares two <b>CHStrings</b> for inequality.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1104b5d3-fac7-4256-9fe5-0dcd428065f6">operator != (CHString, LPCWSTR)</a>
</td>
<td align="left" width="63%">
Compares a <b>CHString</b> with a <b>LPCWSTR</b> for inequality.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a0ba1f3-e862-4210-86a4-55a573e8bb4b">operator []</a>
</td>
<td align="left" width="63%">
Returns the character at a given position — operator substitution for <a href="https://msdn.microsoft.com/ed038b41-211c-4483-99cd-0bc43b241761">GetAt</a>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7ed6379-ccfa-40f9-9607-d9033179b674">operator +</a>
</td>
<td align="left" width="63%">
Concatenates two strings and returns a new string.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/026ff9af-4cda-4261-aa27-e215d49b80ce">operator +=</a>
</td>
<td align="left" width="63%">
Concatenates a new string to the end of an existing string.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bcd0b4a1-4fd1-4d90-b56c-485f1a09f806">operator <  (CHString, LPCWSTR)</a>
</td>
<td align="left" width="63%">
Compares a <b>CHString</b> with a <b>LPCWSTR</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc9b4545-b2a2-48b0-b650-d048860d1386">operator < (CHString, CHString)</a>
</td>
<td align="left" width="63%">
Compares two <b>CHStrings</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21a19f00-67ec-4bf2-b429-44e9463732e4">operator <= (CHString, CHString)</a>
</td>
<td align="left" width="63%">
Compares two <b>CHStrings</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e79b59d-a8fd-4fab-8850-6d95eef08c95">operator <= (CHString, LPCWSTR)</a>
</td>
<td align="left" width="63%">
Compares a <b>CHString</b> with a <b>LPCWSTR</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6864aacf-ac18-4b5a-be3e-3a0d8bb31e74">operator =</a>
</td>
<td align="left" width="63%">
Assigns a new value to a <b>CHString</b> string.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2121ed0a-74e5-4e44-a20e-52f4f895a3ae">operator == (CHString, CHString)</a>
</td>
<td align="left" width="63%">
Compares two <b>CHStrings</b> for equality.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6b1f1c4-6b0d-4a09-9dc1-ad85e00b4707">operator == (CHString, LPCWSTR)</a>
</td>
<td align="left" width="63%">
Compares a <b>CHString</b> with a <b>LPCWSTR</b> for equality.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db9344bb-e0e8-408e-881f-17cea7fc541e">operator > (CHString, CHString)</a>
</td>
<td align="left" width="63%">
Compares two <b>CHStrings</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d364aef-c962-4dc1-b5bc-f6e7a4e2f0c8">operator > (CHString, LPCWSTR)</a>
</td>
<td align="left" width="63%">
Compares a <b>CHString</b> with a <b>LPCWSTR</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f5c43c9-68d5-41f8-a672-ef26d02dadb6">operator >= (CHString, CHString)</a>
</td>
<td align="left" width="63%">
Compares two <b>CHStrings</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/723e83e5-9d52-420d-9850-a145a8b722e9">operator >= (CHString, LPCWSTR)</a>
</td>
<td align="left" width="63%">
Compares a <b>CHString</b> with a <b>LPCWSTR</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7b7575e-e442-487f-9123-c82c471fecdf">operator LPCWSTR</a>
</td>
<td align="left" width="63%">
Directly accesses characters stored in a <b>CHString</b> string as a C-style string.

</td>
</tr>
</table> 


## -remarks



The destructor for the class is <b>CHString::~CHString</b>.



