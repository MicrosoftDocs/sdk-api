---
UID: NF:msime.IFEDictionary.GetPosTable
title: IFEDictionary::GetPosTable (msime.h)
description: Obtains the public POS (Part of Speech) table.
helpviewer_keywords: ["GetPosTable","GetPosTable method [Internationalization for Windows Applications]","GetPosTable method [Internationalization for Windows Applications]","IFEDictionary interface","IFEDictionary interface [Internationalization for Windows Applications]","GetPosTable method","IFEDictionary.GetPosTable","IFEDictionary::GetPosTable","intl.ifedictionary_getpostable","msime/IFEDictionary::GetPosTable"]
old-location: intl\ifedictionary_getpostable.htm
tech.root: Intl
ms.assetid: 0453B37B-A73A-4CD8-AD09-49B9A65B9FD6
ms.date: 12/05/2018
ms.keywords: GetPosTable, GetPosTable method [Internationalization for Windows Applications], GetPosTable method [Internationalization for Windows Applications],IFEDictionary interface, IFEDictionary interface [Internationalization for Windows Applications],GetPosTable method, IFEDictionary.GetPosTable, IFEDictionary::GetPosTable, intl.ifedictionary_getpostable, msime/IFEDictionary::GetPosTable
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
 - IFEDictionary::GetPosTable
 - msime/IFEDictionary::GetPosTable
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
 - IFEDictionary.GetPosTable
---

# IFEDictionary::GetPosTable


## -description

Obtains the public POS (Part of Speech) table.

## -parameters

### -param prgPosTbl [out]

Pointer to the array of <a href="/windows/desktop/api/msime/ns-msime-postbl">POSTBL</a> structures.

### -param pcPosTbl [out]

Pointer to the number of <a href="/windows/desktop/api/msime/ns-msime-postbl">POSTBL</a> structures in the returned array. Can be <b>NULL</b>.

## -returns

<b>S_OK</b> if successful, otherwise <b>E_FAIL</b>.

## -see-also

<a href="/windows/desktop/api/msime/nn-msime-ifedictionary">IFEDictionary</a>



<a href="/windows/desktop/api/msime/ns-msime-postbl">POSTBL</a>