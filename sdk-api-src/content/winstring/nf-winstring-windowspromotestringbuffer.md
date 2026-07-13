---
UID: NF:winstring.WindowsPromoteStringBuffer
title: WindowsPromoteStringBuffer function (winstring.h)
description: Creates an HSTRING from the specified HSTRING_BUFFER.
helpviewer_keywords: ["WindowsPromoteStringBuffer","WindowsPromoteStringBuffer function [Windows Runtime]","winrt.windowspromotestringbuffer","winstring/WindowsPromoteStringBuffer"]
old-location: winrt\windowspromotestringbuffer.htm
tech.root: WinRT
ms.assetid: ac5261fd-2d31-4c65-84f2-4c6b4c3566bb
ms.date: 12/05/2018
ms.keywords: WindowsPromoteStringBuffer, WindowsPromoteStringBuffer function [Windows Runtime], winrt.windowspromotestringbuffer, winstring/WindowsPromoteStringBuffer
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
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WindowsPromoteStringBuffer
 - winstring/WindowsPromoteStringBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComBase.dll
 - API-MS-Win-Core-WinRT-String-l1-1-0.dll
 - API-MS-Win-Core-WinRT-String-L1-1-1.dll
api_name:
 - WindowsPromoteStringBuffer
---

## -description

Creates an [**HSTRING**](/windows/win32/winrt/hstring) from the specified <a href="/windows/desktop/WinRT/hstring-buffer">HSTRING_BUFFER</a>.

## -parameters

### -param bufferHandle

Type: [in] <b><a href="/windows/desktop/WinRT/hstring-buffer">HSTRING_BUFFER</a></b>

The buffer to use for the new [**HSTRING**](/windows/win32/winrt/hstring). You must use the <a href="/windows/desktop/api/winstring/nf-winstring-windowspreallocatestringbuffer">WindowsPreallocateStringBuffer</a> function to create the <a href="/windows/desktop/WinRT/hstring-buffer">HSTRING_BUFFER</a>.

### -param string

Type: [out] <b>[**HSTRING**](/windows/win32/winrt/hstring)*</b>

The newly created [**HSTRING**](/windows/win32/winrt/hstring) that contains the contents of <i>bufferHandle</i>.

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
The <a href="/windows/win32/winrt/hstring"><b>HSTRING</b></a> was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>string</i>  is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>bufferHandle</i> was not created by calling the <a href="/windows/desktop/api/winstring/nf-winstring-windowspreallocatestringbuffer">WindowsPreallocateStringBuffer</a> function, or the caller has overwritten the terminating NULL character in  <i>bufferHandle</i>.

</td>
</tr>
</table>

## -remarks

Use the <b>WindowsPromoteStringBuffer</b> function to create a new [**HSTRING**](/windows/win32/winrt/hstring) from an <a href="/windows/desktop/WinRT/hstring-buffer">HSTRING_BUFFER</a>. Calling the <b>WindowsPromoteStringBuffer</b> function converts the mutable    buffer to an immutable <b>HSTRING</b>. Use the <a href="/windows/desktop/api/winstring/nf-winstring-windowspreallocatestringbuffer">WindowsPreallocateStringBuffer</a> function to create the <b>HSTRING_BUFFER</b>.

If the <b>WindowsPromoteStringBuffer</b> call fails, you can call the <a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestringbuffer">WindowsDeleteStringBuffer</a> function to discard the mutable buffer.

Each call to the <b>WindowsPromoteStringBuffer</b> function must be matched with a corresponding call to <a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a>.

## Examples

The following code example demonstrates how to use the <b>WindowsPromoteStringBuffer</b> function.

```cpp
#include <winstring.h>

int main()
{
    HSTRING hString = NULL;
    HSTRING_BUFFER hStringBuffer = NULL;
    PWSTR strBuffer = NULL;

    HRESULT hr = WindowsPreallocateStringBuffer(10, &strBuffer, &hStringBuffer);

    if (SUCCEEDED(hr))
    {
        // Fill in the buffer

        hr = WindowsPromoteStringBuffer(hStringBuffer, &hString);

        if (SUCCEEDED(hr))
        {
            WindowsDeleteString(hString);
        }
        else
        {
            WindowsDeleteStringBuffer(hStringBuffer);
        }
    }
}
```

## -see-also

[**HSTRING**](/windows/win32/winrt/hstring)

<a href="/windows/desktop/WinRT/hstring-buffer">HSTRING_BUFFER</a>

<a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a>

<a href="/windows/desktop/api/winstring/nf-winstring-windowsdeletestringbuffer">WindowsDeleteStringBuffer</a>

<a href="/windows/desktop/api/winstring/nf-winstring-windowspreallocatestringbuffer">WindowsPreallocateStringBuffer</a>

