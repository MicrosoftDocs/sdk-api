---
UID: NF:msime.IFEDictionary.SetHeader
title: IFEDictionary::SetHeader (msime.h)
description: Sets a dictionary header in a dictionary file.
helpviewer_keywords: ["IFEDictionary interface [Internationalization for Windows Applications]","SetHeader method","IFEDictionary.SetHeader","IFEDictionary::SetHeader","SetHeader","SetHeader method [Internationalization for Windows Applications]","SetHeader method [Internationalization for Windows Applications]","IFEDictionary interface","intl.ifedictionary_setheader","msime/IFEDictionary::SetHeader"]
old-location: intl\ifedictionary_setheader.htm
tech.root: Intl
ms.assetid: 8666DDE7-D90E-4423-984B-EF526FC34320
ms.date: 12/05/2018
ms.keywords: IFEDictionary interface [Internationalization for Windows Applications],SetHeader method, IFEDictionary.SetHeader, IFEDictionary::SetHeader, SetHeader, SetHeader method [Internationalization for Windows Applications], SetHeader method [Internationalization for Windows Applications],IFEDictionary interface, intl.ifedictionary_setheader, msime/IFEDictionary::SetHeader
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFEDictionary::SetHeader
 - msime/IFEDictionary::SetHeader
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
 - IFEDictionary.SetHeader
---

# IFEDictionary::SetHeader


## -description

Sets a dictionary header in a dictionary file.

This method sets or modifies the dictionary header of this <a href="/windows/desktop/api/msime/nn-msime-ifedictionary">IFEDictionary</a> object.

## -parameters

### -param pshf [in]

The <a href="/windows/desktop/api/msime/ns-msime-imeshf">IMESHF</a> header to set.

## -returns

<b>S_OK</b> if successful, otherwise <b>E_FAIL</b>.

## -see-also

<a href="/windows/desktop/api/msime/nn-msime-ifedictionary">IFEDictionary</a>



<a href="/windows/desktop/api/msime/ns-msime-imeshf">IMESHF</a>