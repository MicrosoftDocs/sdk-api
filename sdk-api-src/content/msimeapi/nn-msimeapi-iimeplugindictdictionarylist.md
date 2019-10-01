---
UID: NN:msimeapi.IImePlugInDictDictionaryList
title: IImePlugInDictDictionaryList (msimeapi.h)
author: windows-sdk-content
description: Provides access to the list of IME plug-in dictionaries.
old-location: intl\iimeplugindictdictionarylist.htm
tech.root: Intl
ms.assetid: EF14E963-26DF-4E72-9BDF-3AE99D0B7273
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IImePlugInDictDictionaryList, IImePlugInDictDictionaryList interface [Internationalization for Windows Applications], IImePlugInDictDictionaryList interface [Internationalization for Windows Applications],described, intl.iimeplugindictdictionarylist, msimeapi/IImePlugInDictDictionaryList
ms.topic: interface
f1_keywords: 
 - "msimeapi/IImePlugInDictDictionaryList"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msimeapi.h
api_name:
 - IImePlugInDictDictionaryList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IImePlugInDictDictionaryList interface


## -description


Provides access to the list of IME plug-in dictionaries.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IImePlugInDictDictionaryList</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IImePlugInDictDictionaryList</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/msimeapi/nf-msimeapi-iimeplugindictdictionarylist-deletedictionary">DeleteDictionary</a>
</td>
<td align="left" width="63%">
Deletes a dictionary from the IME's plug-in dictionary list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msimeapi/nf-msimeapi-iimeplugindictdictionarylist-getdictionariesinuse">GetDictionariesInUse</a>
</td>
<td align="left" width="63%">
Obtains the list of Dictionay IDs (<b>GUID</b>) of the IME plug-in dictionaries which are in use by IME, with their creation dates and encryption flags.

</td>
</tr>
</table> 


## -remarks



This interface is implemented in classes of ProgID="ImePlugInDictDictionaryList1041" for Microsoft Japanese IME and ProgID="ImePlugInDictDictionaryList2052" for Microsoft Simplified Chinese IME.



