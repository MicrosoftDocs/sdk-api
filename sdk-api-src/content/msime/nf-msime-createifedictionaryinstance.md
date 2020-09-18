---
UID: NF:msime.CreateIFEDictionaryInstance
title: CreateIFEDictionaryInstance function (msime.h)
description: Returns a pointer to an IFEDictionary interface.
helpviewer_keywords: ["CreateIFEDictionaryInstance","CreateIFEDictionaryInstance function [Internationalization for Windows Applications]","intl.createifedictionaryinstance","msime/CreateIFEDictionaryInstance"]
old-location: intl\createifedictionaryinstance.htm
tech.root: Intl
ms.assetid: 1B762B74-D282-46FE-8202-CA88E478940F
ms.date: 12/05/2018
ms.keywords: CreateIFEDictionaryInstance, CreateIFEDictionaryInstance function [Internationalization for Windows Applications], intl.createifedictionaryinstance, msime/CreateIFEDictionaryInstance
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
 - CreateIFEDictionaryInstance
 - msime/CreateIFEDictionaryInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msime.h
api_name:
 - CreateIFEDictionaryInstance
---

# CreateIFEDictionaryInstance function


## -description

Returns a pointer to an   <a href="/windows/desktop/api/msime/nn-msime-ifedictionary">IFEDictionary</a> interface.

## -parameters

### -param ppvObj [out]

Address of the pointer variable that receives the <a href="/windows/desktop/api/msime/nn-msime-ifedictionary">IFEDictionary</a> interface pointer of the object created.

## -returns

<b>S_OK</b> if successful, otherwise an OLE-defined error code.

## -remarks

There is no import library available that defines this function. It is necessary to manually obtain a pointer to this function using <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.