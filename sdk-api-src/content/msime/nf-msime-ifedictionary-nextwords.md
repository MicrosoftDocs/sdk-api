---
UID: NF:msime.IFEDictionary.NextWords
title: IFEDictionary::NextWords
author: windows-sdk-content
description: Gets the next word entry from a dictionary.
old-location: intl\ifedictionary_nextwords.htm
tech.root: Intl
ms.assetid: 551925ED-B05C-433F-91A9-D2BAC795E783
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: IFEDictionary interface [Internationalization for Windows Applications],NextWords method, IFEDictionary.NextWords, IFEDictionary::NextWords, NextWords, NextWords method [Internationalization for Windows Applications], NextWords method [Internationalization for Windows Applications],IFEDictionary interface, intl.ifedictionary_nextwords, msime/IFEDictionary::NextWords
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msime.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msime.h
api_name:
 - IFEDictionary.NextWords
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFEDictionary::NextWords


## -description


Gets the next word entry from a dictionary.

This method is used only after <a href="https://msdn.microsoft.com/9FEA7E1C-166B-4CA4-B25E-0406AD60AC0B">GetWords</a> to get additional words.


## -parameters




### -param pchBuffer [in, out]

Buffer provided by the caller to receive the data.


### -param cbBuffer [in]

The size of <i>pchBuffer</i>.


### -param pcWrd [out]

The number of <a href="https://msdn.microsoft.com/BC0D039A-7EB4-4A8D-B063-479CF4294FF0">IMEWRD</a> structures returned in <i>pchBuffer</i>. If more entries are found than <i>pchBuffer</i> can store, <b>IFED_S_MORE_ENTRIES</b> will be returned.


## -returns



This method can return one of these values.

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
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IFED_S_MORE_ENTRIES</b></dt>
</dl>
</td>
<td width="60%">
The client must call <a href="https://msdn.microsoft.com/551925ED-B05C-433F-91A9-D2BAC795E783">NextWords</a> to get additional <a href="https://msdn.microsoft.com/BC0D039A-7EB4-4A8D-B063-479CF4294FF0">IMEWRD</a> structures.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9FEA7E1C-166B-4CA4-B25E-0406AD60AC0B">GetWords</a>



<a href="https://msdn.microsoft.com/4C63FF43-0170-4038-AB01-72441E1BB189">IFEDictionary</a>



<a href="https://msdn.microsoft.com/BC0D039A-7EB4-4A8D-B063-479CF4294FF0">IMEWRD</a>
 

 

