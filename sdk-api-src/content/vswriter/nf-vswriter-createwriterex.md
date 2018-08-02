---
UID: NF:vswriter.CreateWriterEx
title: CreateWriterEx function
author: windows-sdk-content
description: This function is reserved for system use.
old-location: base\createwriterex.htm
old-project: VSS
ms.assetid: 044dde5c-599f-495b-8d5c-7a37833bcb41
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CreateWriterEx, CreateWriterEx function, base.createwriterex, vswriter/CreateWriterEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: vswriter.h
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
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - vswriter.h
 - Ext-MS-Win-Fs-VssAPI-L1-1-0.dll
 - VssAPI.dll
api_name:
 - CreateWriterEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# CreateWriterEx function


## -description


This function is reserved for system use. Do not use this function directly. To create a VSS writer, extend the <a href="https://msdn.microsoft.com/29820c1d-2add-402d-a9ca-9e8674d85f7f">CVssWriterEx</a> class. The <b>CVssWriterEx</b> base class implicitly calls <b>CreateWriterEx</b>.


## -parameters




### -param pWriter [in]

Reserved.


### -param pWriterImpl [out]

Reserved.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/29820c1d-2add-402d-a9ca-9e8674d85f7f">CVssWriterEx</a>
 

 

