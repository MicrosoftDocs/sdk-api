---
UID: NN:msime.IFEDictionary
title: IFEDictionary
author: windows-sdk-content
description: The IFEDictionary interface allows clients to access a Microsoft IME user dictionary.
old-location: intl\ifedictionary.htm
old-project: Intl
ms.assetid: 4C63FF43-0170-4038-AB01-72441E1BB189
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IFEDictionary, IFEDictionary interface [Internationalization for Windows Applications], IFEDictionary interface [Internationalization for Windows Applications],described, intl.ifedictionary, msime/IFEDictionary
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msime.h
api_name:
-	IFEDictionary
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IFEDictionary interface


## -description


The <b>IFEDictionary</b> interface allows clients to access a Microsoft IME user dictionary.

This API enables your apps to access and use the data contained in the Microsoft IME dictionaries (including personal name and geographical name dictionaries), or user dictionary. You can develop and sell such applications, provided that:<ul>
<li>You do not create an application that accesses a dictionary that is not a Microsoft IME dictionary through this API.</li>
<li>You do not dump, copy, or distribute the dictionary data contained in the Microsoft IME.</li>
</ul>
You must use this API only for the purpose of developing applications for users who already have the Microsoft IME.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFEDictionary</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFEDictionary</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFEDictionary</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Closes a dictionary file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/218DEE1C-945A-4CD8-BAD5-12F904FAB2DD">Create</a>
</td>
<td align="left" width="63%">
Creates a new dictionary file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5598D1DD-0254-4142-B91F-6BE36DD94228">DisplayProperty</a>
</td>
<td align="left" width="63%">
This method is obsolete starting with Windows 8, and is no longer supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70BBC94A-97D6-4237-A0C9-F6861ED6C95D">ExistWord</a>
</td>
<td align="left" width="63%">
Determines if the specified word exists in <b>IFEDictionary</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DA710A33-BCBC-47B8-857F-5E6DF142C433">GetHeader</a>
</td>
<td align="left" width="63%">
Gets a dictionary header from a dictionary file without opening the dictionary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0453B37B-A73A-4CD8-AD09-49B9A65B9FD6">GetPosTable</a>
</td>
<td align="left" width="63%">
Obtains the public POS (Part of Speech) table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9FEA7E1C-166B-4CA4-B25E-0406AD60AC0B">GetWords</a>
</td>
<td align="left" width="63%">
Gets word entries from a dictionary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/551925ED-B05C-433F-91A9-D2BAC795E783">NextWords</a>
</td>
<td align="left" width="63%">
Gets the next word entry from a dictionary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
</td>
<td align="left" width="63%">
Opens a dictionary file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CD79FBF5-E540-4B5C-A398-B7FE95F86701">RegisterWord</a>
</td>
<td align="left" width="63%">
Registers a new word or deletes an existing word in the <b>IFEDictionary</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8666DDE7-D90E-4423-984B-EF526FC34320">SetHeader</a>
</td>
<td align="left" width="63%">
Sets a dictionary header in a dictionary file.

</td>
</tr>
</table> 


## -remarks



Create an instance of this interface with the <a href="https://msdn.microsoft.com/1B762B74-D282-46FE-8202-CA88E478940F">CreateIFEDictionaryInstance</a> function.



