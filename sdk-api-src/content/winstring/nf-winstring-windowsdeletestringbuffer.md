---
UID: NF:winstring.WindowsDeleteStringBuffer
title: WindowsDeleteStringBuffer function
author: windows-sdk-content
description: Discards a preallocated string buffer if it was not promoted to an HSTRING.
old-location: winrt\windowsdeletestringbuffer.htm
old-project: WinRT
ms.assetid: c543b2ff-56be-48b5-8b44-3d7549c75df2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WindowsDeleteStringBuffer, WindowsDeleteStringBuffer function [Windows Runtime], winrt.windowsdeletestringbuffer, winstring/WindowsDeleteStringBuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WSAVERSION, *PWSAVERSION, *LPWSAVERSION
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
product: Windows
targetos: Windows
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WindowsDeleteStringBuffer function


## -description


Discards a preallocated string buffer if it was not promoted to an <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>.


## -parameters




### -param bufferHandle [in]

Type: <b><a href="https://msdn.microsoft.com/D173CE70-ABF3-4703-A229-0753F2AF6F70">HSTRING_BUFFER</a></b>

The buffer to discard. The <b>WindowsDeleteStringBuffer</b> function raises an exception if  <i>bufferHandle</i> was not allocated by a call to the <a href="https://msdn.microsoft.com/83ebde70-458c-4617-a7fd-a281915f6206">WindowsPreallocateStringBuffer</a> function.


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



Use the <b>WindowsDeleteStringBuffer</b> function to discard a string buffer that was created by the <a href="https://msdn.microsoft.com/83ebde70-458c-4617-a7fd-a281915f6206">WindowsPreallocateStringBuffer</a> function but has not been promoted to an <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a> by the <a href="https://msdn.microsoft.com/ac5261fd-2d31-4c65-84f2-4c6b4c3566bb">WindowsPromoteStringBuffer</a> function.  


<div class="alert"><b>Note</b>  Calling <a href="https://msdn.microsoft.com/ac5261fd-2d31-4c65-84f2-4c6b4c3566bb">WindowsPromoteStringBuffer</a> after calling <b>WindowsDeleteStringBuffer</b> with the same buffer handle is undefined.</div>
<div> </div>



#### Examples

The following code example demonstrates how to use the <b>WindowsDeleteStringBuffer</b> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>int main()
{
    HSTRING_BUFFER hStringBuffer = NULL;
    PWSTR strBuffer = NULL;
    HRESULT hr = WindowsPreallocateStringBuffer(10, &amp;strBuffer, &amp;hStringBuffer);

    // You hit a case in which you need to discard the buffer.

    WindowsStringDeleteBuffer(hStringBuffer);
}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<b></b>



<a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>



<a href="https://msdn.microsoft.com/D173CE70-ABF3-4703-A229-0753F2AF6F70">HSTRING_BUFFER</a>



<a href="https://msdn.microsoft.com/83ebde70-458c-4617-a7fd-a281915f6206">WindowsPreallocateStringBuffer</a>



<a href="https://msdn.microsoft.com/ac5261fd-2d31-4c65-84f2-4c6b4c3566bb">WindowsPromoteStringBuffer</a>
 

 

