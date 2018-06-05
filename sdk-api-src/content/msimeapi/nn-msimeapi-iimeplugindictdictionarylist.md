---
UID: NN:msimeapi.IImePlugInDictDictionaryList
title: IImePlugInDictDictionaryList
author: windows-sdk-content
description: Provides access to the list of IME plug-in dictionaries.
old-location: intl\iimeplugindictdictionarylist.htm
old-project: Intl
ms.assetid: EF14E963-26DF-4E72-9BDF-3AE99D0B7273
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IImePlugInDictDictionaryList, IImePlugInDictDictionaryList interface [Internationalization for Windows Applications], IImePlugInDictDictionaryList interface [Internationalization for Windows Applications],described, intl.iimeplugindictdictionarylist, msimeapi/IImePlugInDictDictionaryList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msimeapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: POSTBL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msimeapi.h
api_name:
-	IImePlugInDictDictionaryList
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IImePlugInDictDictionaryList interface


## -description


Provides access to the list of IME plug-in dictionaries.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IImePlugInDictDictionaryList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IImePlugInDictDictionaryList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IImePlugInDictDictionaryList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38A17092-E545-4018-9D16-2C0406234D62">DeleteDictionary</a>
</td>
<td align="left" width="63%">
Deletes a dictionary from the IME's plug-in dictionary list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/145F403E-7A7D-4336-96CD-620FA61DFCBF">GetDictionariesInUse</a>
</td>
<td align="left" width="63%">
Obtains the list of Dictionay IDs (<b>GUID</b>) of the IME plug-in dictionaries which are in use by IME, with their creation dates and encryption flags.

</td>
</tr>
</table> 


## -remarks



This interface is implemented in classes of ProgID="ImePlugInDictDictionaryList1041" for Microsoft Japanese IME and ProgID="ImePlugInDictDictionaryList2052" for Microsoft Simplified Chinese IME.



