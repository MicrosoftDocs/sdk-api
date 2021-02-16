---
UID: NF:spellcheck.IOptionDescription.get_Labels
title: IOptionDescription::get_Labels (spellcheck.h)
description: Gets the label enumerator for the spell checker option.
old-location: intl\ioptiondescription_labels.htm
tech.root: Intl
ms.assetid: cead418f-2c89-4b7c-a52e-604f5d8685d1
ms.date: 12/05/2018
ms.keywords: IOptionDescription interface [Internationalization for Windows Applications],Labels property, IOptionDescription.Labels, IOptionDescription.get_Labels, IOptionDescription::Labels, IOptionDescription::get_Labels, Labels property [Internationalization for Windows Applications], Labels property [Internationalization for Windows Applications],IOptionDescription interface, get_Labels, intl.ioptiondescription_labels, spellcheck/IOptionDescription::Labels, spellcheck/IOptionDescription::get_Labels
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOptionDescription::get_Labels
 - spellcheck/IOptionDescription::get_Labels
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Spellcheck.h
api_name:
 - IOptionDescription.Labels
 - IOptionDescription.get_Labels
---

# IOptionDescription::get_Labels


## -description

Gets the label enumerator for the spell checker option.

This property is read-only.

## -parameters

## -remarks

When there is a single label, the valid values for this option are 0 (not chosen) and 1 (chosen). When there is more than one label, the first label is associated with the value 0, the second with 1, and so on, effectively forming an enumeration. The labels should be in the language of the spell checker or localized to the user's UI language.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a>



<a href="/windows/desktop/api/spellcheck/nn-spellcheck-ioptiondescription">IOptionDescription</a>