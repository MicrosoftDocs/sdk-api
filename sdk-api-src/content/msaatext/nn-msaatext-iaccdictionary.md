---
UID: NN:msaatext.IAccDictionary
title: IAccDictionary (msaatext.h)
description: Exposes methods for string manipulation.
old-location: winauto\iaccdictionary.htm
tech.root: WinAuto
ms.assetid: 0d18d219-b584-43ff-bded-6ed8f00a252f
ms.date: 12/05/2018
ms.keywords: IAccDictionary, IAccDictionary interface [Windows Accessibility], IAccDictionary interface [Windows Accessibility],described, msaa.iaccdictionary, msaatext/IAccDictionary, winauto.iaccdictionary
ms.topic: interface
f1_keywords:
- msaatext/IAccDictionary
dev_langs:
- c++
req.header: msaatext.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- msaatext.h
api_name:
- IAccDictionary
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAccDictionary interface


## -description


<p class="CCE_Message">[Active Accessibility Text Services is deprecated. Please see     
<a href="https://go.microsoft.com/fwlink/p/?linkid=131573">Microsoft Windows Text Services Framework</a>for more information on advanced text input and natural language technologies.
		]

Exposes methods for string manipulation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccDictionary</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAccDictionary</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccDictionary</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msaatext/nf-msaatext-iaccdictionary-convertvaluetostring">ConvertValueToString</a>
</td>
<td align="left" width="63%">
Converts a property value to a localized string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msaatext/nf-msaatext-iaccdictionary-getlocalizedstring">GetLocalizedString</a>
</td>
<td align="left" width="63%">
Retrieves a localized string for a system property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msaatext/nf-msaatext-iaccdictionary-getmnemonicstring">GetMnemonicString</a>
</td>
<td align="left" width="63%">
Retrieves a mnemonic string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msaatext/nf-msaatext-iaccdictionary-getparentterm">GetParentTerm</a>
</td>
<td align="left" width="63%">
Retrieves the parent object of a specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msaatext/nf-msaatext-iaccdictionary-lookupmnemonicterm">LookupMnemonicTerm</a>
</td>
<td align="left" width="63%">
Retrieves the property for a given mnemonic string.

</td>
</tr>
</table> 

