---
UID: NF:shobjidl_core.IDestinationStreamFactory.GetDestinationStream
title: IDestinationStreamFactory::GetDestinationStream (shobjidl_core.h)
description: Gets an empty stream that receives the new version of the file being copied.
helpviewer_keywords: ["GetDestinationStream","GetDestinationStream method [Windows Shell]","GetDestinationStream method [Windows Shell]","IDestinationStreamFactory interface","IDestinationStreamFactory interface [Windows Shell]","GetDestinationStream method","IDestinationStreamFactory.GetDestinationStream","IDestinationStreamFactory::GetDestinationStream","shell.IDestinationStreamFactory_GetDestinationStream","shell_IDestinationStreamFactory_GetDestinationStream","shobjidl_core/IDestinationStreamFactory::GetDestinationStream"]
old-location: shell\IDestinationStreamFactory_GetDestinationStream.htm
tech.root: shell
ms.assetid: 4903a3a1-12b7-4094-aac8-6e8525998c3c
ms.date: 12/05/2018
ms.keywords: GetDestinationStream, GetDestinationStream method [Windows Shell], GetDestinationStream method [Windows Shell],IDestinationStreamFactory interface, IDestinationStreamFactory interface [Windows Shell],GetDestinationStream method, IDestinationStreamFactory.GetDestinationStream, IDestinationStreamFactory::GetDestinationStream, shell.IDestinationStreamFactory_GetDestinationStream, shell_IDestinationStreamFactory_GetDestinationStream, shobjidl_core/IDestinationStreamFactory::GetDestinationStream
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IDestinationStreamFactory::GetDestinationStream
 - shobjidl_core/IDestinationStreamFactory::GetDestinationStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IDestinationStreamFactory.GetDestinationStream
---

# IDestinationStreamFactory::GetDestinationStream


## -description

Gets an empty stream that receives the new version of the file being copied.

## -parameters

### -param ppstm [out]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>**</b>

The address of a pointer to the new stream.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The property handler author calls <b>IDestinationStreamFactory::GetDestinationStream</b> to get a new empty stream that the new version of the file will write to. The handler builds the destination stream manually, copying from the source stream as necessary.