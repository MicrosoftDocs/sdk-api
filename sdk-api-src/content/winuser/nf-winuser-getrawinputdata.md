---
UID: NF:winuser.GetRawInputData
title: GetRawInputData function
author: windows-sdk-content
description: Retrieves the raw input from the specified device.
old-location: inputdev\getrawinputdata.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\rawinput\rawinputreference\rawinputfunctions\getrawinputdata.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRawInputData, GetRawInputData function [Keyboard and Mouse Input], RID_HEADER, RID_INPUT, _win32_GetRawInputData, _win32_getrawinputdata_cpp, inputdev.getrawinputdata, winui._win32_getrawinputdata, winuser/GetRawInputData
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
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-RTCore-NTUser-Rawinput-L1-1-0.dll
 - MinUser.dll
api_name:
 - GetRawInputData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetRawInputData function


## -description


Retrieves the raw input from the specified device.


## -parameters




### -param hRawInput [in]

Type: <b>HRAWINPUT</b>

A handle to the <a href="https://msdn.microsoft.com/ee238c20-c3a5-4b6b-af13-727ea18fb448">RAWINPUT</a> structure. This comes from the 
					<i>lParam</i> in <a href="https://msdn.microsoft.com/a014d68c-841c-4120-b752-4b3fac60e12d">WM_INPUT</a>. 


### -param uiCommand [in]

Type: <b>UINT</b>

The command flag. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RID_HEADER"></a><a id="rid_header"></a><dl>
<dt><b>RID_HEADER</b></dt>
<dt>0x10000005</dt>
</dl>
</td>
<td width="60%">
Get the header information from the <a href="https://msdn.microsoft.com/ee238c20-c3a5-4b6b-af13-727ea18fb448">RAWINPUT</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="RID_INPUT"></a><a id="rid_input"></a><dl>
<dt><b>RID_INPUT</b></dt>
<dt>0x10000003</dt>
</dl>
</td>
<td width="60%">
Get the raw data from the <a href="https://msdn.microsoft.com/ee238c20-c3a5-4b6b-af13-727ea18fb448">RAWINPUT</a> structure.

</td>
</tr>
</table>
 


### -param pData [out, optional]

Type: <b>LPVOID</b>

A pointer to the data that comes from the <a href="https://msdn.microsoft.com/ee238c20-c3a5-4b6b-af13-727ea18fb448">RAWINPUT</a> structure. This depends on the value of 
					<i>uiCommand</i>. If 
					<i>pData</i> is <b>NULL</b>, the required size of the buffer is returned in *<i>pcbSize</i>. 


### -param pcbSize [in, out]

Type: <b>PUINT</b>

The size, in bytes, of the data in 
					<i>pData</i>. 


### -param cbSizeHeader [in]

Type: <b>UINT</b>

The size, in bytes, of the <a href="https://msdn.microsoft.com/abc4226a-679a-4963-af8e-e87670e60126">RAWINPUTHEADER</a> structure. 


## -returns



Type: <b>UINT</b>

If 
						<i>pData</i> is <b>NULL</b> and the function is successful, the return value is 0. If 
						<i>pData</i> is not <b>NULL</b> and the function is successful, the return value is the number of bytes copied into pData.

If there is an error, the return value is (<b>UINT</b>)-1.




## -remarks



<b>GetRawInputData</b> gets the raw input one <a href="https://msdn.microsoft.com/ee238c20-c3a5-4b6b-af13-727ea18fb448">RAWINPUT</a> structure at a time. In contrast, <a href="https://msdn.microsoft.com/a76d9b93-4faa-43c4-b72e-2ca9fc306703">GetRawInputBuffer</a> gets an array of <b>RAWINPUT</b> structures.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/a76d9b93-4faa-43c4-b72e-2ca9fc306703">GetRawInputBuffer</a>



<a href="https://msdn.microsoft.com/ee238c20-c3a5-4b6b-af13-727ea18fb448">RAWINPUT</a>



<a href="https://msdn.microsoft.com/abc4226a-679a-4963-af8e-e87670e60126">RAWINPUTHEADER</a>



<a href="https://msdn.microsoft.com/a2afdb80-d68a-4c33-826f-96739d239cd9">Raw Input</a>



<b>Reference</b>
 

 

