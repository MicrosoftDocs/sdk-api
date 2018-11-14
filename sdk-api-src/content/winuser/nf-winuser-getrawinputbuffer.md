---
UID: NF:winuser.GetRawInputBuffer
title: GetRawInputBuffer function
author: windows-sdk-content
description: Performs a buffered read of the raw input data.
old-location: inputdev\getrawinputbuffer.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputfunctions\getrawinputbuffer.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetRawInputBuffer, GetRawInputBuffer function [Keyboard and Mouse Input], _win32_GetRawInputBuffer, _win32_getrawinputbuffer_cpp, inputdev.getrawinputbuffer, winui._win32_getrawinputbuffer, winuser/GetRawInputBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetRawInputBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetRawInputBuffer
: 
---

# GetRawInputBuffer function


## -description


Performs a buffered read of the raw input data.


## -parameters




### -param pData [out, optional]

Type: <b>PRAWINPUT</b>

A pointer to a buffer of <a href="https://msdn.microsoft.com/ee238c20-c3a5-4b6b-af13-727ea18fb448">RAWINPUT</a> structures that contain the raw input data. If <b>NULL</b>, the minimum required buffer, in bytes, is returned in *<i>pcbSize</i>. 


### -param pcbSize [in, out]

Type: <b>PUINT</b>

The size, in bytes, of a <a href="https://msdn.microsoft.com/ee238c20-c3a5-4b6b-af13-727ea18fb448">RAWINPUT</a> structure. 


### -param cbSizeHeader [in]

Type: <b>UINT</b>

The size, in bytes, of the <a href="https://msdn.microsoft.com/abc4226a-679a-4963-af8e-e87670e60126">RAWINPUTHEADER</a> structure. 


## -returns



Type: <b>UINT</b>

If 
						<i>pData</i> is NULL and the function is successful, the return value is zero. If 
						<i>pData</i> is not NULL and the function is successful, the return value is the number of <a href="https://msdn.microsoft.com/ee238c20-c3a5-4b6b-af13-727ea18fb448">RAWINPUT</a> structures written to 
						<i>pData</i>.

If an error occurs, the return value is (<b>UINT</b>)-1. Call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> for the error code.




## -remarks



Using <b>GetRawInputBuffer</b>, the raw input data is buffered in the array of <a href="https://msdn.microsoft.com/ee238c20-c3a5-4b6b-af13-727ea18fb448">RAWINPUT</a> structures. For an unbuffered read, use the <a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a> function to read in the raw input data. 

The <a href="https://msdn.microsoft.com/63ce135b-9d79-4ed7-a0fd-aec5c4559b5e">NEXTRAWINPUTBLOCK</a> macro allows an application to traverse an array of <a href="https://msdn.microsoft.com/ee238c20-c3a5-4b6b-af13-727ea18fb448">RAWINPUT</a> structures.

<div class="alert"><b>Note</b>  To get the correct size of the raw input buffer, do not use *<i>pcbSize</i>, use *<i>pcbSize</i> * 8 instead.   To ensure <b>GetRawInputBuffer</b> behaves properly on WOW64, you must align the <a href="https://msdn.microsoft.com/ee238c20-c3a5-4b6b-af13-727ea18fb448">RAWINPUT</a> structure by 8 bytes. The following code shows how to align <b>RAWINPUT</b>  for WOW64.  <div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>[StructLayout(LayoutKind.Explicit)]
internal struct RAWINPUT
{
    [FieldOffset(0)]
    public RAWINPUTHEADER header;

    [FieldOffset(16+8)]
    public RAWMOUSE mouse;

    [FieldOffset(16+8)]
    public RAWKEYBOARD keyboard;

    [FieldOffset(16+8)]
    public RAWHID hid;
}
</pre>
</td>
</tr>
</table></span></div>
</div>
<div> </div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e92266a7-86ac-43f4-b0eb-762e145a1017">GetMessage</a>



<a href="https://msdn.microsoft.com/63ce135b-9d79-4ed7-a0fd-aec5c4559b5e">NEXTRAWINPUTBLOCK</a>



<a href="https://msdn.microsoft.com/ee238c20-c3a5-4b6b-af13-727ea18fb448">RAWINPUT</a>



<a href="https://msdn.microsoft.com/abc4226a-679a-4963-af8e-e87670e60126">RAWINPUTHEADER</a>



<a href="https://msdn.microsoft.com/a2afdb80-d68a-4c33-826f-96739d239cd9">Raw Input</a>



<b>Reference</b>
 

 

