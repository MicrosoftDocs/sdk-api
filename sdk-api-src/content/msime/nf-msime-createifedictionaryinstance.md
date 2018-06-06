---
UID: NF:msime.CreateIFEDictionaryInstance
title: CreateIFEDictionaryInstance function
author: windows-sdk-content
description: Returns a pointer to an IFEDictionary interface.
old-location: intl\createifedictionaryinstance.htm
old-project: Intl
ms.assetid: 1B762B74-D282-46FE-8202-CA88E478940F
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: CreateIFEDictionaryInstance, CreateIFEDictionaryInstance function [Internationalization for Windows Applications], intl.createifedictionaryinstance, msime/CreateIFEDictionaryInstance
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: IMEUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msime.h
api_name:
 - CreateIFEDictionaryInstance
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CreateIFEDictionaryInstance function


## -description


Returns a pointer to an   <a href="https://msdn.microsoft.com/4C63FF43-0170-4038-AB01-72441E1BB189">IFEDictionary</a> interface.


## -parameters




### -param ppvObj [out]

Address of the pointer variable that receives the <a href="https://msdn.microsoft.com/4C63FF43-0170-4038-AB01-72441E1BB189">IFEDictionary</a> interface pointer of the object created.


## -returns



<b>S_OK</b> if successful, otherwise an OLE-defined error code.




## -remarks



There is no import library available that defines this function. It is necessary to manually obtain a pointer to this function using <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>.



