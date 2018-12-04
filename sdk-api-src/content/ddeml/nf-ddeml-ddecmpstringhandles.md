---
UID: NF:ddeml.DdeCmpStringHandles
title: DdeCmpStringHandles function
author: windows-sdk-content
description: Compares the values of two string handles. The value of a string handle is not related to the case of the associated string.
old-location: dataxchg\ddecmpstringhandles.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddecmpstringhandles.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: DdeCmpStringHandles, DdeCmpStringHandles function [Data Exchange], _win32_DdeCmpStringHandles, _win32_ddecmpstringhandles_cpp, dataxchg.ddecmpstringhandles, ddeml/DdeCmpStringHandles, winui._win32_ddecmpstringhandles
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - DdeCmpStringHandles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



<a href="https://msdn.microsoft.com/7695d435-3bb4-4041-8992-9155efa8911e">DdeAccessData</a>



<a href="https://msdn.microsoft.com/561bbf80-cc73-4fe1-ba95-837d515834eb">DdeCreateStringHandle</a>



<a href="https://msdn.microsoft.com/93228467-345b-4ff1-942e-2d75a53bce65">DdeFreeStringHandle</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

