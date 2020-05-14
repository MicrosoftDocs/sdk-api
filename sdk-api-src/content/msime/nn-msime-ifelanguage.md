---
UID: NN:msime.IFELanguage
title: IFELanguage (msime.h)
description: The IFELanguage interface provides language processing services using the Microsoft IME.helpviewer_keywords: ["IFELanguage","IFELanguage interface [Internationalization for Windows Applications]","IFELanguage interface [Internationalization for Windows Applications]","described","intl.ifelanguage","msime/IFELanguage"]
old-location: intl\ifelanguage.htm
tech.root: Intl
ms.assetid: 9EE1BD9E-2D58-4720-841C-39865375BFE0
ms.date: 12/05/2018
ms.keywords: IFELanguage, IFELanguage interface [Internationalization for Windows Applications], IFELanguage interface [Internationalization for Windows Applications],described, intl.ifelanguage, msime/IFELanguage
f1_keywords:
- msime/IFELanguage
dev_langs:
- c++
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
- IFELanguage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFELanguage interface


## -description


The <b>IFELanguage</b> interface provides language processing services using the Microsoft IME.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFELanguage</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFELanguage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFELanguage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifelanguage-close">Close</a>
</td>
<td align="left" width="63%">
Terminates the <b>IFELanguage</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifelanguage-getconversion">GetConversion</a>
</td>
<td align="left" width="63%">
Converts the input string (which usually contains the Hiragana character) to converted strings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifelanguage-getconversionmodecaps">GetConversionModeCaps</a>
</td>
<td align="left" width="63%">
Gets the conversion mode capability of the <b>IFELanguage</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifelanguage-getjmorphresult">GetJMorphResult</a>
</td>
<td align="left" width="63%">
Gets morphological analysis results.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-ifelanguage-open">Open</a>
</td>
<td align="left" width="63%">
Initializes the <b>IFELanguage</b> object.

</td>
</tr>
</table> 


## -remarks



Create an instance of this interface with the <a href="https://docs.microsoft.com/windows/desktop/api/msime/nf-msime-createifelanguageinstance">CreateIFELanguageInstance</a> function.



