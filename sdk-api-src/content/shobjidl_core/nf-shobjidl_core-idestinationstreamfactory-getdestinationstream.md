---
UID: NF:shobjidl_core.IDestinationStreamFactory.GetDestinationStream
title: IDestinationStreamFactory::GetDestinationStream
author: windows-sdk-content
description: Gets an empty stream that receives the new version of the file being copied.
old-location: shell\IDestinationStreamFactory_GetDestinationStream.htm
old-project: shell
ms.assetid: 4903a3a1-12b7-4094-aac8-6e8525998c3c
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: GetDestinationStream, GetDestinationStream method [Windows Shell], GetDestinationStream method [Windows Shell],IDestinationStreamFactory interface, IDestinationStreamFactory interface [Windows Shell],GetDestinationStream method, IDestinationStreamFactory.GetDestinationStream, IDestinationStreamFactory::GetDestinationStream, shell.IDestinationStreamFactory_GetDestinationStream, shell_IDestinationStreamFactory_GetDestinationStream, shobjidl_core/IDestinationStreamFactory::GetDestinationStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IDestinationStreamFactory.GetDestinationStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IDestinationStreamFactory::GetDestinationStream


## -description


Gets an empty stream that receives the new version of the file being copied.


## -parameters




### -param ppstm [out]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>**</b>

The address of a pointer to the new stream.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The property handler author calls <b>IDestinationStreamFactory::GetDestinationStream</b> to get a new empty stream that the new version of the file will write to. The handler builds the destination stream manually, copying from the source stream as necessary.



