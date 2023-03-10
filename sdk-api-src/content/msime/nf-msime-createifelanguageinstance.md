---
UID: NF:msime.CreateIFELanguageInstance
title: CreateIFELanguageInstance function (msime.h)
description: Returns a pointer to an IFELanguage interface.
helpviewer_keywords: ["CreateIFELanguageInstance","CreateIFELanguageInstance function [Internationalization for Windows Applications]","intl.createifelanguageinstance","msime/CreateIFELanguageInstance"]
old-location: intl\createifelanguageinstance.htm
tech.root: Intl
ms.assetid: DF79C260-F43B-4580-B252-6D906C235CD4
ms.date: 12/05/2018
ms.keywords: CreateIFELanguageInstance, CreateIFELanguageInstance function [Internationalization for Windows Applications], intl.createifelanguageinstance, msime/CreateIFELanguageInstance
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
 - CreateIFELanguageInstance
 - msime/CreateIFELanguageInstance
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
 - CreateIFELanguageInstance
---

# CreateIFELanguageInstance function


## -description

Returns a pointer to an   <a href="/windows/desktop/api/msime/nn-msime-ifelanguage">IFELanguage</a> interface.

## -parameters

### -param clsid [in]

Reserved. Must be set to <b>NULL</b>.

### -param ppvObj [out]

Address of the pointer variable that receives the <a href="/windows/desktop/api/msime/nn-msime-ifelanguage">IFELanguage</a> interface pointer of the object created.

## -returns

<b>S_OK</b> if successful, otherwise an OLE-defined error code.