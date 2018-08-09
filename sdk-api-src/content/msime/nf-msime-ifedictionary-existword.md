---
UID: NF:msime.IFEDictionary.ExistWord
title: IFEDictionary::ExistWord
author: windows-sdk-content
description: Determines if the specified word exists in IFEDictionary.
old-location: intl\ifedictionary_existword.htm
old-project: Intl
ms.assetid: 70BBC94A-97D6-4237-A0C9-F6861ED6C95D
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ExistWord, ExistWord method [Internationalization for Windows Applications], ExistWord method [Internationalization for Windows Applications],IFEDictionary interface, IFEDictionary interface [Internationalization for Windows Applications],ExistWord method, IFEDictionary.ExistWord, IFEDictionary::ExistWord, intl.ifedictionary_existword, msime/IFEDictionary::ExistWord
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: IMEUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msime.h
api_name:
 - IFEDictionary.ExistWord
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IFEDictionary::ExistWord


## -description


Determines if the specified word exists in <a href="https://msdn.microsoft.com/4C63FF43-0170-4038-AB01-72441E1BB189">IFEDictionary</a>.


## -parameters




### -param pwrd [in]

An <a href="https://msdn.microsoft.com/BC0D039A-7EB4-4A8D-B063-479CF4294FF0">IMEWRD</a> structure specifying the word to check.


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
<td width="60%">
The word exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The word does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4C63FF43-0170-4038-AB01-72441E1BB189">IFEDictionary</a>



<a href="https://msdn.microsoft.com/BC0D039A-7EB4-4A8D-B063-479CF4294FF0">IMEWRD</a>
 

 

