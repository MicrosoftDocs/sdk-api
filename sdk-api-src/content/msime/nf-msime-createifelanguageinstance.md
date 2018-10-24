---
UID: NF:msime.CreateIFELanguageInstance
title: CreateIFELanguageInstance function
author: windows-sdk-content
description: Returns a pointer to an IFELanguage interface.
old-location: intl\createifelanguageinstance.htm
tech.root: Intl
ms.assetid: DF79C260-F43B-4580-B252-6D906C235CD4
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CreateIFELanguageInstance, CreateIFELanguageInstance function [Internationalization for Windows Applications], intl.createifelanguageinstance, msime/CreateIFELanguageInstance
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
 - CreateIFELanguageInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateIFELanguageInstance function


## -description


Returns a pointer to an   <a href="https://msdn.microsoft.com/9EE1BD9E-2D58-4720-841C-39865375BFE0">IFELanguage</a> interface.


## -parameters




### -param clsid [in]

Reserved. Must be set to <b>NULL</b>.


### -param ppvObj [out]

Address of the pointer variable that receives the <a href="https://msdn.microsoft.com/9EE1BD9E-2D58-4720-841C-39865375BFE0">IFELanguage</a> interface pointer of the object created.


## -returns



<b>S_OK</b> if successful, otherwise an OLE-defined error code.



