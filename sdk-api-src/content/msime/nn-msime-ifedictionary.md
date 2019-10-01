---
UID: NN:msime.IFEDictionary
title: IFEDictionary (msime.h)
author: windows-sdk-content
description: The IFEDictionary interface allows clients to access a Microsoft IME user dictionary.
old-location: intl\ifedictionary.htm
tech.root: Intl
ms.assetid: 4C63FF43-0170-4038-AB01-72441E1BB189
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFEDictionary, IFEDictionary interface [Internationalization for Windows Applications], IFEDictionary interface [Internationalization for Windows Applications],described, intl.ifedictionary, msime/IFEDictionary
ms.topic: interface
f1_keywords: 
 - "msime/IFEDictionary"
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
 - IFEDictionary
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFEDictionary interface


## -description


The <b>IFEDictionary</b> interface allows clients to access a Microsoft IME user dictionary.

This API enables your apps to access and use the data contained in the Microsoft IME dictionaries (including personal name and geographical name dictionaries), or user dictionary. You can develop and sell such applications, provided that:<ul>
<li>You do not create an application that accesses a dictionary that is not a Microsoft IME dictionary through this API.</li>
<li>You do not dump, copy, or distribute the dictionary data contained in the Microsoft IME.</li>
</ul>You must use this API only for the purpose of developing applications for users who already have the Microsoft IME.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFEDictionary</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFEDictionary</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifedictionary-close">Close</a>
</td>
<td align="left" width="63%">
Closes a dictionary file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifedictionary-create">Create</a>
</td>
<td align="left" width="63%">
Creates a new dictionary file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifedictionary-displayproperty">DisplayProperty</a>
</td>
<td align="left" width="63%">
This method is obsolete starting with Windows 8, and is no longer supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifedictionary-existword">ExistWord</a>
</td>
<td align="left" width="63%">
Determines if the specified word exists in <b>IFEDictionary</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifedictionary-getheader">GetHeader</a>
</td>
<td align="left" width="63%">
Gets a dictionary header from a dictionary file without opening the dictionary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifedictionary-getpostable">GetPosTable</a>
</td>
<td align="left" width="63%">
Obtains the public POS (Part of Speech) table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifedictionary-getwords">GetWords</a>
</td>
<td align="left" width="63%">
Gets word entries from a dictionary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifedictionary-nextwords">NextWords</a>
</td>
<td align="left" width="63%">
Gets the next word entry from a dictionary.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifedictionary-open">Open</a>
</td>
<td align="left" width="63%">
Opens a dictionary file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifedictionary-registerword">RegisterWord</a>
</td>
<td align="left" width="63%">
Registers a new word or deletes an existing word in the <b>IFEDictionary</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifedictionary-setheader">SetHeader</a>
</td>
<td align="left" width="63%">
Sets a dictionary header in a dictionary file.

</td>
</tr>
</table> 


## -remarks



Create an instance of this interface with the <a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-createifedictionaryinstance">CreateIFEDictionaryInstance</a> function.



