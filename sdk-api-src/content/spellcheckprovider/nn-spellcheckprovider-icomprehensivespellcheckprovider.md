---
UID: NN:spellcheckprovider.IComprehensiveSpellCheckProvider
title: IComprehensiveSpellCheckProvider (spellcheckprovider.h)
description: Allows the provider to optionally support a more comprehensive spell checking functionality.
helpviewer_keywords: ["IComprehensiveSpellCheckProvider","IComprehensiveSpellCheckProvider interface [Internationalization for Windows Applications]","IComprehensiveSpellCheckProvider interface [Internationalization for Windows Applications]","described","intl.icomprehensivespellcheckprovider","spellcheckprovider/IComprehensiveSpellCheckProvider"]
old-location: intl\icomprehensivespellcheckprovider.htm
tech.root: Intl
ms.assetid: 303EE887-DCF0-4575-A45F-5A4088DE8F7B
ms.date: 12/05/2018
ms.keywords: IComprehensiveSpellCheckProvider, IComprehensiveSpellCheckProvider interface [Internationalization for Windows Applications], IComprehensiveSpellCheckProvider interface [Internationalization for Windows Applications],described, intl.icomprehensivespellcheckprovider, spellcheckprovider/IComprehensiveSpellCheckProvider
f1_keywords:
- spellcheckprovider/IComprehensiveSpellCheckProvider
dev_langs:
- c++
req.header: spellcheckprovider.h
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
- spellcheckprovider.h
api_name:
- IComprehensiveSpellCheckProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComprehensiveSpellCheckProvider interface


## -description


Allows the provider to optionally support a more comprehensive spell checking functionality.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComprehensiveSpellCheckProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComprehensiveSpellCheckProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComprehensiveSpellCheckProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Intl/icomprehensivespellcheckprovider-comprehensivecheck">ComprehensiveCheck</a>
</td>
<td align="left" width="63%">
Spell-check the provider text in a more thorough manner than <a href="https://docs.microsoft.com/windows/desktop/api/spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check">ISpellCheckProvider::Check</a>.

</td>
</tr>
</table> 

