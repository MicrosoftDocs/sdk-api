---
UID: NL:chstring.CHString
title: CHString (chstring.h)
description: The following table lists the CHString methods.
old-location: wmi\chstring.htm
tech.root: WmiSdk
ms.assetid: e2e4378f-d842-4bca-bffc-a60e718caed3
ms.date: 12/05/2018
ms.keywords: ??1CHString@@QAE@XZ, ??1CHString@@QEAA@XZ, CHString, CHString class [Windows Management Instrumentation], CHString class [Windows Management Instrumentation],described, _hmm_chstring, chstring/CHString, wmi.chstring
f1_keywords:
- chstring/CHString
dev_langs:
- c++
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
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
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
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-chstring(constchstring_)">CHString</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-allocsysstring">AllocSysString</a>
</td>
<td align="left" width="63%">
Allocates a BSTR from <b>CHString</b> data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-collate">Collate</a>
</td>
<td align="left" width="63%">
Compares two strings (case sensitive; uses locale-specific information).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-compare">Compare</a>
</td>
<td align="left" width="63%">
Compares two strings (case sensitive).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-comparenocase">CompareNoCase</a>
</td>
<td align="left" width="63%">
Compares two strings (case insensitive).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-empty">Empty</a>
</td>
<td align="left" width="63%">
Forces a string to have 0 (zero) length.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-find(wchar)">Find</a>
</td>
<td align="left" width="63%">Overloaded. Finds a character or substring inside a larger string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-findoneof">FindOneOf</a>
</td>
<td align="left" width="63%">
Finds the first matching character from a set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-format(uint_---)">Format</a>
</td>
<td align="left" width="63%">Overloaded. Formats the string as <b>sprintf</b> does.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-formatmessagew(uint_---)">FormatMessageW</a>
</td>
<td align="left" width="63%">Overloaded. Formats a message string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-formatv">FormatV</a>
</td>
<td align="left" width="63%">
Formats the string as <b>vsprintf</b> does.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-freeextra">FreeExtra</a>
</td>
<td align="left" width="63%">
Removes any overhead of this string by freeing any extra memory previously allocated to the string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-getalloclength">GetAllocLength</a>
</td>
<td align="left" width="63%">
Returns the size of the string buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-getat(int)">GetAt</a>
</td>
<td align="left" width="63%">Overloaded. Returns the character at a given position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-getbuffer">GetBuffer</a>
</td>
<td align="left" width="63%">
Returns a pointer to the characters in the <b>CHString</b> string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-getbuffersetlength">GetBufferSetLength</a>
</td>
<td align="left" width="63%">
Returns a pointer to the characters in the <b>CHString</b> string, truncating to the specified length.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-getdata">GetData</a>
</td>
<td align="left" width="63%">
Returns a pointer to the data in the <b>CHString</b> string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Returns the number of Unicode characters in a <b>CHString</b> string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-isempty">IsEmpty</a>
</td>
<td align="left" width="63%">
Tests whether a <b>CHString</b> string contains no characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-left">Left</a>
</td>
<td align="left" width="63%">
Extracts the left part of a string (like the Basic <b>LEFT$</b> function).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-loadstringw(uint)">LoadStringW</a>
</td>
<td align="left" width="63%">
Loads an existing <b>CHString</b> string from a resource file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-lockbuffer">LockBuffer</a>
</td>
<td align="left" width="63%">
Disables reference counting and protects the string in the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-makelower">MakeLower</a>
</td>
<td align="left" width="63%">
Converts all of the characters in this string to lowercase characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-makereverse">MakeReverse</a>
</td>
<td align="left" width="63%">
Reverses the characters in this string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-makeupper">MakeUpper</a>
</td>
<td align="left" width="63%">
Converts all of the characters in this string to uppercase characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-mid(int_int)">Mid</a>
</td>
<td align="left" width="63%">Overloaded. Extracts the middle part of a string (like the Basic <b>MID$</b> function).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-releasebuffer">ReleaseBuffer</a>
</td>
<td align="left" width="63%">
Releases control of the buffer returned by <a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-getbuffer">GetBuffer</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-reversefind">ReverseFind</a>
</td>
<td align="left" width="63%">
Finds a character inside a larger string; starts from the end.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-right">Right</a>
</td>
<td align="left" width="63%">
Extracts the right part of a string (like the Basic <b>RIGHT$</b> function).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-setat">SetAt</a>
</td>
<td align="left" width="63%">
Sets a character at a given position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-spanexcluding">SpanExcluding</a>
</td>
<td align="left" width="63%">
Extracts a substring that contains only the characters that are not in the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-spanincluding">SpanIncluding</a>
</td>
<td align="left" width="63%">
Extracts a substring that contains only the characters in a set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-trimleft">TrimLeft</a>
</td>
<td align="left" width="63%">
Trims leading whitespace characters from the string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-trimright">TrimRight</a>
</td>
<td align="left" width="63%">
Trims trailing whitespace characters from the string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-unlockbuffer">UnlockBuffer</a>
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa385704(v=vs.85)">operator != (CHString, CHString)</a>
</td>
<td align="left" width="63%">
Compares two <b>CHStrings</b> for inequality.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa385763(v=vs.85)">operator != (CHString, LPCWSTR)</a>
</td>
<td align="left" width="63%">
Compares a <b>CHString</b> with a <b>LPCWSTR</b> for inequality.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa386162(v=vs.85)">operator []</a>
</td>
<td align="left" width="63%">
Returns the character at a given position — operator substitution for <a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-getat(int)">GetAt</a>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring--operator-plus">operator +</a>
</td>
<td align="left" width="63%">
Concatenates two strings and returns a new string.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring--operator-plus-equal">operator +=</a>
</td>
<td align="left" width="63%">
Concatenates a new string to the end of an existing string.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa385695(v=vs.85)">operator <  (CHString, LPCWSTR)</a>
</td>
<td align="left" width="63%">
Compares a <b>CHString</b> with a <b>LPCWSTR</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa385689(v=vs.85)">operator < (CHString, CHString)</a>
</td>
<td align="left" width="63%">
Compares two <b>CHStrings</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa385676(v=vs.85)">operator <= (CHString, CHString)</a>
</td>
<td align="left" width="63%">
Compares two <b>CHStrings</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa385683(v=vs.85)">operator <= (CHString, LPCWSTR)</a>
</td>
<td align="left" width="63%">
Compares a <b>CHString</b> with a <b>LPCWSTR</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/chstring--operator-equal">operator =</a>
</td>
<td align="left" width="63%">
Assigns a new value to a <b>CHString</b> string.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa385641(v=vs.85)">operator == (CHString, CHString)</a>
</td>
<td align="left" width="63%">
Compares two <b>CHStrings</b> for equality.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa385645(v=vs.85)">operator == (CHString, LPCWSTR)</a>
</td>
<td align="left" width="63%">
Compares a <b>CHString</b> with a <b>LPCWSTR</b> for equality.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa385665(v=vs.85)">operator > (CHString, CHString)</a>
</td>
<td align="left" width="63%">
Compares two <b>CHStrings</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa385672(v=vs.85)">operator > (CHString, LPCWSTR)</a>
</td>
<td align="left" width="63%">
Compares a <b>CHString</b> with a <b>LPCWSTR</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa385652(v=vs.85)">operator >= (CHString, CHString)</a>
</td>
<td align="left" width="63%">
Compares two <b>CHStrings</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa385661(v=vs.85)">operator >= (CHString, LPCWSTR)</a>
</td>
<td align="left" width="63%">
Compares a <b>CHString</b> with a <b>LPCWSTR</b>.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/chstring/nf-chstring-chstring-operatorlpcwstr">operator LPCWSTR</a>
</td>
<td align="left" width="63%">
Directly accesses characters stored in a <b>CHString</b> string as a C-style string.

</td>
</tr>
</table> 


## -remarks



The destructor for the class is <b>CHString::~CHString</b>.



