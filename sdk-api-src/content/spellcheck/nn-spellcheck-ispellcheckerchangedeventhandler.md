---
UID: NN:spellcheck.ISpellCheckerChangedEventHandler
title: ISpellCheckerChangedEventHandler
author: windows-sdk-content
description: Allows the caller to create a handler for notifications that the state of the speller has changed.
old-location: intl\ispellcheckerchangedeventhandler.htm
tech.root: Intl
ms.assetid: 9dd1f768-a901-4682-9530-019fe1dfbf0b
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ISpellCheckerChangedEventHandler, ISpellCheckerChangedEventHandler interface [Internationalization for Windows Applications], ISpellCheckerChangedEventHandler interface [Internationalization for Windows Applications],described, intl.ispellcheckerchangedeventhandler, spellcheck/ISpellCheckerChangedEventHandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: spellcheck.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Spellcheck.idl
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
 - Spellcheck.h
api_name:
 - ISpellCheckerChangedEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpellCheckerChangedEventHandler interface


## -description


Allows the caller to create a handler for notifications that the state of the speller has changed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpellCheckerChangedEventHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpellCheckerChangedEventHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpellCheckerChangedEventHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/585f147f-b644-4b6a-81d6-8ffeeb39d76a">Invoke</a>
</td>
<td align="left" width="63%">
Receives the SpellCheckerChanged event.

</td>
</tr>
</table> 

