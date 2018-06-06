---
UID: NE:winnls._NORM_FORM
title: "_NORM_FORM"
author: windows-sdk-content
description: Specifies the supported normalization forms.
old-location: intl\norm_form.htm
old-project: Intl
ms.assetid: d0133c6d-3534-4616-8b6f-07ec712808a3
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: NORM_FORM, NORM_FORM enumeration [Internationalization for Windows Applications], NormalizationC, NormalizationD, NormalizationKC, NormalizationKD, NormalizationOther, _NORM_FORM, _win32_NORM_FORM, intl.norm_form, winnls/NORM_FORM, winnls/NormalizationC, winnls/NormalizationD, winnls/NormalizationKC, winnls/NormalizationKD, winnls/NormalizationOther
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
req.typenames: NORM_FORM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnls.h
api_name:
 - NORM_FORM
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _NORM_FORM enumeration


## -description


Specifies the supported normalization forms.


## -enum-fields




### -field NormalizationOther

Not supported.


### -field NormalizationC

Unicode normalization form C, canonical composition. Transforms each decomposed grouping, consisting of a base character plus combining characters, to the canonical precomposed equivalent. For example, A + ¨ becomes Ä.


### -field NormalizationD

Unicode normalization form D, canonical decomposition. Transforms each precomposed character to its canonical decomposed equivalent. For example, Ä becomes A + ¨.


### -field NormalizationKC

Unicode normalization form KC, compatibility composition. Transforms each base plus combining characters to the canonical precomposed equivalent and all compatibility characters to their equivalents. For example, the ligature ﬁ becomes f + i; similarly, A + ¨ + ﬁ + n becomes Ä + f + i + n.


### -field NormalizationKD

Unicode normalization form KD, compatibility decomposition. Transforms each precomposed character to its canonical decomposed equivalent and all compatibility characters to their equivalents. For example, Ä + ﬁ + n becomes A + ¨ + f + i + n.


## -remarks




        For more information about the normalization forms, see <a href="https://msdn.microsoft.com/027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35">Using Unicode Normalization to Represent Strings</a>.




## -see-also




<a href="https://msdn.microsoft.com/5a1d3977-9fe9-457f-b0a2-46b32bcc27db">IsNormalizedString</a>



<a href="https://msdn.microsoft.com/93911b65-e2ba-432d-9c65-53dd57687077">National Language Support Enumeration Types</a>



<a href="https://msdn.microsoft.com/ef76d0e5-2999-4a21-8522-c698013e3816">NormalizeString</a>



<a href="https://msdn.microsoft.com/027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35">Using Unicode Normalization to Represent Strings</a>
 

 

