---
UID: NF:winstring.WindowsCompareStringOrdinal
title: WindowsCompareStringOrdinal function (winstring.h)
description: Compares two specified HSTRING objects and returns an integer that indicates their relative position in a sort order.
helpviewer_keywords: ["WindowsCompareStringOrdinal","WindowsCompareStringOrdinal function [Windows Runtime]","winrt.windowscomparestringordinal","winstring/WindowsCompareStringOrdinal"]
old-location: winrt\windowscomparestringordinal.htm
tech.root: WinRT
ms.assetid: 40B34A65-4E3C-4B9D-9315-A0EF015BB8D0
ms.date: 12/05/2018
ms.keywords: WindowsCompareStringOrdinal, WindowsCompareStringOrdinal function [Windows Runtime], winrt.windowscomparestringordinal, winstring/WindowsCompareStringOrdinal
req.header: winstring.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WinRTType.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WindowsCompareStringOrdinal
 - winstring/WindowsCompareStringOrdinal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WinRTType.lib
 - WinRTType.dll
 - API-MS-Win-Core-WinRT-String-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-WinRT-String-L1-1-1.dll
api_name:
 - WindowsCompareStringOrdinal
---

## -description

Compares two specified [**HSTRING**](/windows/win32/winrt/hstring) objects and returns an integer that indicates their relative position in a sort order.

## -parameters

### -param string1

Type: [in] **[HSTRING](/windows/win32/winrt/hstring)**

The first string to compare.

### -param string2

Type: [in] **[HSTRING](/windows/win32/winrt/hstring)**

The second string to compare.

### -param result

Type: [out] <b>INT32*</b>

A value that indicates the lexical relationship between <i>string1</i> and <i>string2</i>.

## -returns

Type: <b>HRESULT</b>

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The  comparison was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>result</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Use the <b>WindowsCompareStringOrdinal</b> function to compare two [**HSTRING**](/windows/win32/winrt/hstring) objects. After the comparison completes, the  <i>result</i> out parameter contains one of three values.

<table>
<tr>
<th>Value</th>
<th>Condition</th>
</tr>
<tr>
<td>-1</td>
<td><i>string1</i> is less than <i>string2</i>.</td>
</tr>
<tr>
<td>0</td>
<td><i>string1</i> equals <i>string2</i>.</td>
</tr>
<tr>
<td>1</td>
<td><i>string1</i> is greater than <i>string2</i>.</td>
</tr>
</table>

