---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WindowsPromoteStringBuffer function


## -description


Creates an <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a> from the specified <a href="https://msdn.microsoft.com/D173CE70-ABF3-4703-A229-0753F2AF6F70">HSTRING_BUFFER</a>.


## -parameters




### -param bufferHandle [in]

Type: <b><a href="https://msdn.microsoft.com/D173CE70-ABF3-4703-A229-0753F2AF6F70">HSTRING_BUFFER</a></b>

The buffer to use for the new <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>. You must use the <a href="https://msdn.microsoft.com/83ebde70-458c-4617-a7fd-a281915f6206">WindowsPreallocateStringBuffer</a> function to create the <a href="https://msdn.microsoft.com/D173CE70-ABF3-4703-A229-0753F2AF6F70">HSTRING_BUFFER</a>.


### -param string [out]

Type: <b><a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>*</b>

The newly created <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a> that contains the contents of <i>bufferHandle</i>.


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
The  <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a> was created successfully.

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
<i>bufferHandle</i> was not created by calling the <a href="https://msdn.microsoft.com/83ebde70-458c-4617-a7fd-a281915f6206">WindowsPreallocateStringBuffer</a> function, or the caller has overwritten the   terminating NUL character in  <i>bufferHandle</i>.

</td>
</tr>
</table>
 




## -remarks



Use the <b>WindowsPromoteStringBuffer</b> function to create a new <a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a> from an <a href="https://msdn.microsoft.com/D173CE70-ABF3-4703-A229-0753F2AF6F70">HSTRING_BUFFER</a>. Calling the <b>WindowsPromoteStringBuffer</b> function converts the mutable    buffer to an immutable <b>HSTRING</b>. Use the <a href="https://msdn.microsoft.com/83ebde70-458c-4617-a7fd-a281915f6206">WindowsPreallocateStringBuffer</a> function to create the <b>HSTRING_BUFFER</b>.

If the <b>WindowsPromoteStringBuffer</b> call fails, you can call the <a href="https://msdn.microsoft.com/c543b2ff-56be-48b5-8b44-3d7549c75df2">WindowsDeleteStringBuffer</a> function to discard the mutable buffer.

Each call to the <b>WindowsPromoteStringBuffer</b> function must be matched with a corresponding call to <a href="https://msdn.microsoft.com/79B9E5CF-396C-45FB-931B-7B50281A0446">WindowsDeleteString</a>.


#### Examples

The following code example demonstrates how to use the <b>WindowsPromoteStringBuffer</b> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;WinrtString.h&gt;

int main()
{
    HSTRING hString = NULL;
    LPVOID* hStringBuffer = NULL;
    PWSTR strBuffer = NULL;

    HRESULT hr = WindowsPreallocateStringBuffer(10, &amp;strBuffer, &amp;hStringBuffer);

    if (SUCCEEDED(hr))
    {
        // Fill in the buffer

        hr = WindowsPromoteStringBuffer(hStringBuffer, &amp;hString);

        If (SUCCEEDED(hr)
        {
            WindowsDeleteString(hString);
        }
        else
	       {
            WindowsDeleteStringBuffer(hStringBuffer);
	       }
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<b></b>



<a href="https://msdn.microsoft.com/763ACE57-EFDD-482E-851E-668D7756C5DF">HSTRING</a>



<a href="https://msdn.microsoft.com/D173CE70-ABF3-4703-A229-0753F2AF6F70">HSTRING_BUFFER</a>



<a href="https://msdn.microsoft.com/79B9E5CF-396C-45FB-931B-7B50281A0446">WindowsDeleteString</a>



<a href="https://msdn.microsoft.com/c543b2ff-56be-48b5-8b44-3d7549c75df2">WindowsDeleteStringBuffer</a>



<a href="https://msdn.microsoft.com/83ebde70-458c-4617-a7fd-a281915f6206">WindowsPreallocateStringBuffer</a>
 

 

