---
UID: NN:imapi2.IDiscFormat2Erase
title: IDiscFormat2Erase (imapi2.h)
description: Use this interface to erase data from a disc.
helpviewer_keywords: ["IDiscFormat2Erase","IDiscFormat2Erase interface [IMAPI]","IDiscFormat2Erase interface [IMAPI]","described","imapi.idiscformat2erase","imapi2/IDiscFormat2Erase"]
old-location: imapi\idiscformat2erase.htm
tech.root: imapi
ms.assetid: 3789c876-f42c-4f69-b683-96c157d6418d
ms.date: 12/05/2018
ms.keywords: IDiscFormat2Erase, IDiscFormat2Erase interface [IMAPI], IDiscFormat2Erase interface [IMAPI],described, imapi.idiscformat2erase, imapi2/IDiscFormat2Erase
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - IDiscFormat2Erase
 - imapi2/IDiscFormat2Erase
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscFormat2Erase
---

# IDiscFormat2Erase interface


## -description

Use this interface to erase data from a disc.

To create an instance of this interface, call the <b>CoCreateInstance</b> function. Use__uuidof(MsftDiscFormat2Erase) for the class identifier and __uuidof(IDiscFormat2Erase) for the interface identifier.

## -inheritance

The <b>IDiscFormat2Erase</b> interface inherits from <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2">IDiscFormat2</a>. <b>IDiscFormat2Erase</b> also has these types of members:

## -remarks

To create the <b>MsftDiscFormat2Erase</b> object in a script, use IMAPI2.MsftDiscFormat2Erase as the program identifier when calling <b>CreateObject</b>.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2">IDiscFormat2</a>
