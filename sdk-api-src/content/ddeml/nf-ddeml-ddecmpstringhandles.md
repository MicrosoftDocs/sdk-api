---
UID: NF:ddeml.DdeCmpStringHandles
title: DdeCmpStringHandles function
author: windows-sdk-content
description: Compares the values of two string handles. The value of a string handle is not related to the case of the associated string.
old-location: dataxchg\ddecmpstringhandles.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddecmpstringhandles.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DdeCmpStringHandles, DdeCmpStringHandles function [Data Exchange], _win32_DdeCmpStringHandles, _win32_ddecmpstringhandles_cpp, dataxchg.ddecmpstringhandles, ddeml/DdeCmpStringHandles, winui._win32_ddecmpstringhandles
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ddeml.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DDEPOKE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - DdeCmpStringHandles
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
---

# DdeCmpStringHandles function


## -description


Compares the values of two string handles. The value of a string handle is not related to the case of the associated string. 


## -parameters




### -param hsz1 [in]

Type: <b>HSZ</b>

A handle to the first string. 


### -param hsz2 [in]

Type: <b>HSZ</b>

A handle to the second string. 


## -returns



Type: <b>int</b>

The return value can be one of the following values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
The value of <i>hsz1</i> is either 0 or less than the value of <i>hsz2</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The values of <i>hsz1</i> and <i>hsz2</i> are equal (both can be 0).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The value of <i>hsz2</i> is either 0 or less than the value of <i>hsz1</i>.

</td>
</tr>
</table>
 




## -remarks



An application that must do a case-sensitive comparison of two string handles should compare the string handles directly. An application should use <b>DdeCmpStringHandles</b> for all other comparisons to preserve the case-insensitive nature of Dynamic Data Exchange (DDE). 

<b>DdeCmpStringHandles</b> cannot be used to sort string handles alphabetically. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648740(v=VS.85).aspx">DdeAccessData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648748(v=VS.85).aspx">DdeCreateStringHandle</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648753(v=VS.85).aspx">DdeFreeStringHandle</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648712(v=VS.85).aspx">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

