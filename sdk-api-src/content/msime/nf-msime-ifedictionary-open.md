---
UID: NF:msime.IFEDictionary.Open
title: IFEDictionary::Open (msime.h)
description: Opens a dictionary file.
helpviewer_keywords: ["IFEDictionary interface [Internationalization for Windows Applications]","Open method","IFEDictionary.Open","IFEDictionary::Open","Open","Open method [Internationalization for Windows Applications]","Open method [Internationalization for Windows Applications]","IFEDictionary interface","intl.ifedictionary_open","msime/IFEDictionary::Open"]
old-location: intl\ifedictionary_open.htm
tech.root: Intl
ms.assetid: 7170EED5-0D96-4314-8B9F-A019052B0F32
ms.date: 12/05/2018
ms.keywords: IFEDictionary interface [Internationalization for Windows Applications],Open method, IFEDictionary.Open, IFEDictionary::Open, Open, Open method [Internationalization for Windows Applications], Open method [Internationalization for Windows Applications],IFEDictionary interface, intl.ifedictionary_open, msime/IFEDictionary::Open
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
 - IFEDictionary::Open
 - msime/IFEDictionary::Open
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
 - IFEDictionary.Open
---

# IFEDictionary::Open


## -description

Opens a dictionary file.

This method opens an existing dictionary file and associates it with this <a href="/windows/desktop/api/msime/nn-msime-ifedictionary">IFEDictionary</a> object. To implement a multiple dictionary facility, multiple open and release procedures must be carried out.

## -parameters

### -param pchDictPath [in, optional]

Points to a <b>NULL</b>-terminated file name string to be opened. If <i>pchDictPath</i> is <b>NULL</b> or an empty string, the user dictionary opened by the IME kernel will be used. If <i>pchDictPath</i> is an empty string, the name of user dictionary will be copied into <i>pchDictPath</i>, in which case the size of <i>pchDictPath</i> must be <b>MAX_PATH</b>.

### -param pshf [out]

The <a href="/windows/desktop/api/msime/ns-msime-imeshf">IMESHF</a> header of the opened file. Can be <b>NULL</b>.

## -returns

One of the following:

<ul>
<li><b>S_OK</b></li>
<li><b>JDIC_S_EMPTY_DICTIONARY</b></li>
<li><b>IFED_E_NOT_FOUND</b></li>
<li><b>IFED_E_INVALID_FORMAT</b></li>
<li><b>IFED_E_OPEN_FAILED</b></li>
<li><b>E_FAIL</b></li>
</ul>

## -see-also

<a href="/windows/desktop/api/msime/nn-msime-ifedictionary">IFEDictionary</a>



<a href="/windows/desktop/api/msime/ns-msime-imeshf">IMESHF</a>