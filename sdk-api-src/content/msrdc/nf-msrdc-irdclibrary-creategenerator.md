---
UID: NF:msrdc.IRdcLibrary.CreateGenerator
title: IRdcLibrary::CreateGenerator
author: windows-sdk-content
description: Creates a signature generator that will generate the specified levels of signatures.
old-location: rdc\irdclibrary_creategenerator.htm
tech.root: Rdc
ms.assetid: 9cd64c3f-acd7-4e59-916f-90e90f452e12
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateGenerator, CreateGenerator method [Remote Differential Compression], CreateGenerator method [Remote Differential Compression],IRdcLibrary interface, IRdcLibrary interface [Remote Differential Compression],CreateGenerator method, IRdcLibrary.CreateGenerator, IRdcLibrary::CreateGenerator, fs.irdclibrary_creategenerator, msrdc/IRdcLibrary::CreateGenerator, rdc.irdclibrary_creategenerator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsRdc.dll
req.lib: 
req.dll: MsRdc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - IRdcLibrary.CreateGenerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRdcLibrary::CreateGenerator


## -description


The <b>CreateGenerator</b> method
   creates a signature generator that will generate the specified levels of signatures.


## -parameters




### -param depth [in]

The number of levels of signatures to generate. The valid range is from 
    <b>MSRDC_MINIMUM_DEPTH</b> to <b>MSRDC_MAXIMUM_DEPTH</b>.


### -param iGeneratorParametersArray [in]

Pointer to an array of initialized 
    <a href="https://msdn.microsoft.com/1b2db5c5-79eb-490a-ae03-36b0e926725d">IRdcGeneratorParameters</a> interface pointers. Each 
    <b>IRdcGeneratorParameters</b> interface pointer would 
    have been initialized by 
    <a href="https://msdn.microsoft.com/a39e26bc-7493-4def-af6d-cf3620ec8a9f">IRdcLibrary::CreateGeneratorParameters</a> or 
    <a href="https://msdn.microsoft.com/c2ee5aea-c186-4017-bc35-2f83f5c05824">IRdcGenerator::GetGeneratorParameters</a>.


### -param iGenerator [out]

Pointer to a location that will receive the returned 
      <a href="https://msdn.microsoft.com/0288318a-0974-4870-b423-87c52090eb33">IRdcGenerator</a> interface pointer. Callers must release the 
      interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a39e26bc-7493-4def-af6d-cf3620ec8a9f">CreateGeneratorParameters</a>



<a href="https://msdn.microsoft.com/1b2db5c5-79eb-490a-ae03-36b0e926725d">IRdcGeneratorParameters</a>



<a href="https://msdn.microsoft.com/941fa35c-20fa-4843-89be-26112ff7eec5">IRdcLibrary</a>



<a href="https://msdn.microsoft.com/6fbced31-a230-44d4-a9ee-bb3e15df2563">OpenGeneratorParameters</a>
 

 

