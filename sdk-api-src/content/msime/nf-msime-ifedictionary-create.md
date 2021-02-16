---
UID: NF:msime.IFEDictionary.Create
title: IFEDictionary::Create (msime.h)
description: Creates a new dictionary file.
helpviewer_keywords: ["Create","Create method [Internationalization for Windows Applications]","Create method [Internationalization for Windows Applications]","IFEDictionary interface","IFEDictionary interface [Internationalization for Windows Applications]","Create method","IFEDictionary.Create","IFEDictionary::Create","intl.ifedictionary_create","msime/IFEDictionary::Create"]
old-location: intl\ifedictionary_create.htm
tech.root: Intl
ms.assetid: 218DEE1C-945A-4CD8-BAD5-12F904FAB2DD
ms.date: 12/05/2018
ms.keywords: Create, Create method [Internationalization for Windows Applications], Create method [Internationalization for Windows Applications],IFEDictionary interface, IFEDictionary interface [Internationalization for Windows Applications],Create method, IFEDictionary.Create, IFEDictionary::Create, intl.ifedictionary_create, msime/IFEDictionary::Create
req.header: msime.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFEDictionary::Create
 - msime/IFEDictionary::Create
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msime.h
api_name:
 - IFEDictionary.Create
---

# IFEDictionary::Create


## -description

Creates a new dictionary file.

## -parameters

### -param pchDictPath [in]

A <b>NULL</b>-terminated string containing the path and name for the new dictionary file to be created.

### -param pshf [in]

The <a href="/windows/desktop/api/msime/ns-msime-imeshf">IMESHF</a> header for the new dictionary.

## -returns

One of the following:

<ul>
<li><b>S_OK</b></li>
<li><b>IFED_S_EMPTY_DICTIONARY</b></li>
<li><b>E_OUTOFMEMORY</b></li>
<li><b>E_FAIL</b></li>
</ul>

## -see-also

<a href="/windows/desktop/api/msime/nn-msime-ifedictionary">IFEDictionary</a>



<a href="/windows/desktop/api/msime/ns-msime-imeshf">IMESHF</a>