---
UID: NF:spellcheck.ISpellingError.get_Replacement
title: ISpellingError::get_Replacement
author: windows-sdk-content
description: Gets the text to use as replacement text when the corrective action is replace.
old-location: intl\ispellingerror_replacement.htm
tech.root: Intl
ms.assetid: df161212-8950-4d05-9f69-15165fea9da9
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: ISpellingError interface [Internationalization for Windows Applications],Replacement property, ISpellingError.Replacement, ISpellingError.get_Replacement, ISpellingError::Replacement, ISpellingError::get_Replacement, Replacement property [Internationalization for Windows Applications], Replacement property [Internationalization for Windows Applications],ISpellingError interface, get_Replacement, intl.ispellingerror_replacement, spellcheck/ISpellingError::Replacement, spellcheck/ISpellingError::get_Replacement
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ISpellingError.Replacement
 - ISpellingError.get_Replacement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpellingError::get_Replacement


## -description


Gets the text to use as replacement text when the corrective action is replace.

This property is read-only.


## -parameters


## -remarks



If the <a href="https://msdn.microsoft.com/370CF89E-97BF-4AB5-8AD6-3B2DF08463E0">CORRECTIVE_ACTION</a> returned by <a href="https://msdn.microsoft.com/9b28d194-01a3-4ea2-8428-d2e91e6abad8">CorrectiveAction</a> is not <b>CORRECTIVE_ACTION_REPLACE</b>, <i>value</i> is the empty string.




## -see-also




<a href="https://msdn.microsoft.com/370CF89E-97BF-4AB5-8AD6-3B2DF08463E0">CORRECTIVE_ACTION</a>



<a href="https://msdn.microsoft.com/9b28d194-01a3-4ea2-8428-d2e91e6abad8">CorrectiveAction</a>



<a href="https://msdn.microsoft.com/90a233a4-44a4-4f8f-92bb-ea65fa213616">ISpellingError</a>
 

 

