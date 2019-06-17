---
UID: NF:winstring.WindowsPreallocateStringBuffer
title: WindowsPreallocateStringBuffer function (winstring.h)
author: windows-sdk-content
description: Allocates a mutable character buffer for use in HSTRING creation.
old-location: winrt\windowspreallocatestringbuffer.htm
tech.root: WinRT
ms.assetid: 83ebde70-458c-4617-a7fd-a281915f6206
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WindowsPreallocateStringBuffer, WindowsPreallocateStringBuffer function [Windows Runtime], winrt.windowspreallocatestringbuffer, winstring/WindowsPreallocateStringBuffer
ms.topic: function
f1_keywords: ["winstring/WindowsPreallocateStringBuffer"]
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
 - WindowsPreallocateStringBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WindowsPreallocateStringBuffer function


## -description


Allocates a mutable character buffer for use in <a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a> creation.


## -parameters




### -param length [in]

Type: <b>UINT32</b>

The size of the buffer to allocate. A value of zero corresponds to the empty string.


### -param charBuffer [out]

Type: <b>WCHAR**</b>

The mutable buffer that holds the characters. Note that the buffer already contains a terminating <b>NULL</b> character.


### -param bufferHandle [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring-buffer">HSTRING_BUFFER</a>*</b>

The preallocated string buffer, or <b>NULL</b> if  <i>length</i> is 0.


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
The  <a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a> was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>mutableBuffer</i> or <i>bufferHandle</i>  is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MEM_E_INVALID_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The requested <a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a> allocation size is too large.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the <a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a> buffer.

</td>
</tr>
</table>
 




## -remarks



Use the <b>WindowsPreallocateStringBuffer</b> function to create a mutable character buffer that you can manipulate prior to committing it to  an immutable <a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a>. When you have finished populating the <i>mutableBuffer</i> with your string, call the <a href="https://docs.microsoft.com/windows/desktop/api/winstring/nf-winstring-windowspromotestringbuffer">WindowsPromoteStringBuffer</a>  function with the <i>bufferHandle</i> parameter  to create the <b>HSTRING</b>. You must write exactly <i>length</i> characters into the buffer.

Call the <a href="https://docs.microsoft.com/windows/desktop/api/winstring/nf-winstring-windowsdeletestringbuffer">WindowsDeleteStringBuffer</a> function to discard the mutable buffer prior to promotion. If the buffer has already been promoted by a call to <a href="https://docs.microsoft.com/windows/desktop/api/winstring/nf-winstring-windowspromotestringbuffer">WindowsPromoteStringBuffer</a>, call the <a href="https://docs.microsoft.com/windows/desktop/api/winstring/nf-winstring-windowsdeletestring">WindowsDeleteString</a> function to discard the string. If the <b>WindowsPromoteStringBuffer</b> call fails, you can call the <b>WindowsDeleteStringBuffer</b> function to discard the mutable buffer.




#### Examples

The following code example demonstrates how to use the <b>WindowsPreallocateStringBuffer</b> function.


```cpp
#include <WinrtString.h>

int main()
{
    HSTRING hString = NULL;
    HSTRING_BUFFER hStringBuffer = NULL;
    PWSTR strBuffer = NULL;

    HRESULT hr = WindowsPreallocateStringBuffer(10, &strBuffer, &hStringBuffer);

    if (SUCCEEDED(hr))
    {
        hr = WindowsPromoteStringBuffer(hStringBuffer, &hString);
    }

    WindowsDeleteString(hString);  
}

```





## -see-also




<b></b>



<a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a>



<a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring-buffer">HSTRING_BUFFER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winstring/nf-winstring-windowsdeletestringbuffer">WindowsDeleteStringBuffer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winstring/nf-winstring-windowspromotestringbuffer">WindowsPromoteStringBuffer</a>
 

 

