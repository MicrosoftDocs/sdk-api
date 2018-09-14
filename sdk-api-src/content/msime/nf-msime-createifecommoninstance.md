---
UID: NF:msime.CreateIFECommonInstance
title: CreateIFECommonInstance function
author: windows-sdk-content
description: Returns a pointer to an IFECommon interface.
old-location: intl\createifecommoninstance.htm
tech.root: Intl
ms.assetid: A8A0CCC4-0A60-4E2A-9E6D-DC2C614B631D
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CreateIFECommonInstance, CreateIFECommonInstance function [Internationalization for Windows Applications], intl.createifecommoninstance, msime/CreateIFECommonInstance
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msime.h
api_name:
 - CreateIFECommonInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateIFECommonInstance function


## -description


Returns a pointer to an   <a href="https://msdn.microsoft.com/9FBECA6F-F162-485D-938F-FADC2D47083E">IFECommon</a> interface.


## -parameters




### -param ppvObj [out]

Address of the pointer variable that receives the <a href="https://msdn.microsoft.com/9FBECA6F-F162-485D-938F-FADC2D47083E">IFECommon</a> interface pointer of the object created.


## -returns



<b>S_OK</b> if successful, otherwise an OLE-defined error code.




## -remarks



There is no import library available that defines this function. It is necessary to manually obtain a pointer to this function using <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>.



