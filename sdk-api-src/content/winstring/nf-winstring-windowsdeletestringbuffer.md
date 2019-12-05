---
UID: NF:winstring.WindowsDeleteStringBuffer
title: WindowsDeleteStringBuffer function (winstring.h)
description: Discards a preallocated string buffer if it was not promoted to an HSTRING.
old-location: winrt\windowsdeletestringbuffer.htm
tech.root: WinRT
ms.assetid: c543b2ff-56be-48b5-8b44-3d7549c75df2
ms.date: 12/05/2018
ms.keywords: WindowsDeleteStringBuffer, WindowsDeleteStringBuffer function [Windows Runtime], winrt.windowsdeletestringbuffer, winstring/WindowsDeleteStringBuffer
ms.topic: function
f1_keywords:
- winstring/WindowsDeleteStringBuffer
dev_langs:
- c++
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
- WindowsDeleteStringBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WindowsDeleteStringBuffer function


## -description


Discards a preallocated string buffer if it was not promoted to an <a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a>.


## -parameters




### -param bufferHandle [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring-buffer">HSTRING_BUFFER</a></b>

The buffer to discard. The <b>WindowsDeleteStringBuffer</b> function raises an exception if  <i>bufferHandle</i> was not allocated by a call to the <a href="https://docs.microsoft.com/windows/desktop/api/winstring/nf-winstring-windowspreallocatestringbuffer">WindowsPreallocateStringBuffer</a> function.


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
The  buffer was discarded successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>bufferHandle</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



Use the <b>WindowsDeleteStringBuffer</b> function to discard a string buffer that was created by the <a href="https://docs.microsoft.com/windows/desktop/api/winstring/nf-winstring-windowspreallocatestringbuffer">WindowsPreallocateStringBuffer</a> function but has not been promoted to an <a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a> by the <a href="https://docs.microsoft.com/windows/desktop/api/winstring/nf-winstring-windowspromotestringbuffer">WindowsPromoteStringBuffer</a> function.  


<div class="alert"><b>Note</b>  Calling <a href="https://docs.microsoft.com/windows/desktop/api/winstring/nf-winstring-windowspromotestringbuffer">WindowsPromoteStringBuffer</a> after calling <b>WindowsDeleteStringBuffer</b> with the same buffer handle is undefined.</div>
<div> </div>



#### Examples

The following code example demonstrates how to use the <b>WindowsDeleteStringBuffer</b> function.


```cpp
int main()
{
    HSTRING_BUFFER hStringBuffer = NULL;
    PWSTR strBuffer = NULL;
    HRESULT hr = WindowsPreallocateStringBuffer(10, &strBuffer, &hStringBuffer);

    // You hit a case in which you need to discard the buffer.

    WindowsStringDeleteBuffer(hStringBuffer);
}


```





## -see-also




<b></b>



<a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring">HSTRING</a>



<a href="https://docs.microsoft.com/windows/desktop/WinRT/hstring-buffer">HSTRING_BUFFER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winstring/nf-winstring-windowspreallocatestringbuffer">WindowsPreallocateStringBuffer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winstring/nf-winstring-windowspromotestringbuffer">WindowsPromoteStringBuffer</a>
 

 

