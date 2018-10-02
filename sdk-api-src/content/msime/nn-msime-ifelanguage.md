---
UID: NN:msime.IFELanguage
title: IFELanguage
author: windows-sdk-content
description: The IFELanguage interface provides language processing services using the Microsoft IME.
old-location: intl\ifelanguage.htm
tech.root: Intl
ms.assetid: 9EE1BD9E-2D58-4720-841C-39865375BFE0
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IFELanguage, IFELanguage interface [Internationalization for Windows Applications], IFELanguage interface [Internationalization for Windows Applications],described, intl.ifelanguage, msime/IFELanguage
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFELanguage interface


## -description


The <b>IFELanguage</b> interface provides language processing services using the Microsoft IME.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFELanguage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFELanguage</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/EF03C40A-62D1-4B8E-9960-3CD2D515B7CE">Close</a>
</td>
<td align="left" width="63%">
Terminates the <b>IFELanguage</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A1FA36C7-6A1A-4B08-BA29-7F7C8FE8DF16">GetConversion</a>
</td>
<td align="left" width="63%">
Converts the input string (which usually contains the Hiragana character) to converted strings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B1A3D121-C650-4D04-9278-791A12F73A2E">GetConversionModeCaps</a>
</td>
<td align="left" width="63%">
Gets the conversion mode capability of the <b>IFELanguage</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CCE546B2-88CE-4B54-8EBF-FCA2C5ADFBB4">GetJMorphResult</a>
</td>
<td align="left" width="63%">
Gets morphological analysis results.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2E1CEC6B-B0EA-4DBE-A122-D44606B467CC">Open</a>
</td>
<td align="left" width="63%">
Initializes the <b>IFELanguage</b> object.

</td>
</tr>
</table> 


## -remarks



Create an instance of this interface with the <a href="https://msdn.microsoft.com/DF79C260-F43B-4580-B252-6D906C235CD4">CreateIFELanguageInstance</a> function.



