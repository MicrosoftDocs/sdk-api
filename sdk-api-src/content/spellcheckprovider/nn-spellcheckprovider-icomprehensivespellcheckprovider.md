---
UID: NN:spellcheckprovider.IComprehensiveSpellCheckProvider
title: IComprehensiveSpellCheckProvider
author: windows-driver-content
description: Allows the provider to optionally support a more comprehensive spell checking functionality.
old-location: intl\icomprehensivespellcheckprovider.htm
old-project: Intl
ms.assetid: 303EE887-DCF0-4575-A45F-5A4088DE8F7B
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IComprehensiveSpellCheckProvider, IComprehensiveSpellCheckProvider interface [Internationalization for Windows Applications], IComprehensiveSpellCheckProvider interface [Internationalization for Windows Applications],described, intl.icomprehensivespellcheckprovider, spellcheckprovider/IComprehensiveSpellCheckProvider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: WORDLIST_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	spellcheckprovider.h
api_name:
-	IComprehensiveSpellCheckProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IComprehensiveSpellCheckProvider interface


## -description


Allows the provider to optionally support a more comprehensive spell checking functionality.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComprehensiveSpellCheckProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComprehensiveSpellCheckProvider</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/BD334EB8-4E14-478D-AB2A-E7F863C4BE0F">ComprehensiveCheck</a>
</td>
<td align="left" width="63%">
Spell-check the provider text in a more thorough manner than <a href="https://msdn.microsoft.com/B8C62B56-FF72-4C94-AC77-A6BEFCFE2589">ISpellCheckProvider::Check</a>.

</td>
</tr>
</table> 

