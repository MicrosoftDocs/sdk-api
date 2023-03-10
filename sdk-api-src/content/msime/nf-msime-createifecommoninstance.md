---
UID: NF:msime.CreateIFECommonInstance
title: CreateIFECommonInstance function (msime.h)
description: Returns a pointer to an IFECommon interface.
helpviewer_keywords: ["CreateIFECommonInstance","CreateIFECommonInstance function [Internationalization for Windows Applications]","intl.createifecommoninstance","msime/CreateIFECommonInstance"]
old-location: intl\createifecommoninstance.htm
tech.root: Intl
ms.assetid: A8A0CCC4-0A60-4E2A-9E6D-DC2C614B631D
ms.date: 12/05/2018
ms.keywords: CreateIFECommonInstance, CreateIFECommonInstance function [Internationalization for Windows Applications], intl.createifecommoninstance, msime/CreateIFECommonInstance
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
 - CreateIFECommonInstance
 - msime/CreateIFECommonInstance
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
 - CreateIFECommonInstance
---

# CreateIFECommonInstance function


## -description

Returns a pointer to an   <a href="/windows/desktop/api/msime/nn-msime-ifecommon">IFECommon</a> interface.

## -parameters

### -param ppvObj [out]

Address of the pointer variable that receives the <a href="/windows/desktop/api/msime/nn-msime-ifecommon">IFECommon</a> interface pointer of the object created.

## -returns

<b>S_OK</b> if successful, otherwise an OLE-defined error code.

## -remarks

There is no import library available that defines this function. It is necessary to manually obtain a pointer to this function using <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>.