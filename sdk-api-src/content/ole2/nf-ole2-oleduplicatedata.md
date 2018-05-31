---
UID: NF:ole2.OleDuplicateData
title: OleDuplicateData function
author: windows-sdk-content
description: Duplicates the data found in the specified handle and returns a handle to the duplicated data. The source data is in a clipboard format. Use this function to help implement some of the data transfer interfaces such as IDataObject.
old-location: com\oleduplicatedata.htm
old-project: com
ms.assetid: c4ba0b54-e9e1-4c05-b4f8-ce5390cada17
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: OleDuplicateData, OleDuplicateData function [COM], _ole_OleDuplicateData, com.oleduplicatedata, ole2/OleDuplicateData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ole2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: QACONTROL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
api_name:
-	OleDuplicateData
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# OleDuplicateData function


## -description


Duplicates the data found in the specified handle and returns a handle to the duplicated data. The source data is in a clipboard format. Use this function to help implement some of the data transfer interfaces such as <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>.


## -parameters




### -param hSrc [in]

 Handle of the source data.


### -param cfFormat [in]

Clipboard format of the source data.


### -param uiFlags [in]

Flags to be used to allocate global memory for the copied data. These flags are passed to GlobalAlloc. If the value of <i>uiFlags</i> is <b>NULL</b>, GMEM_MOVEABLE is used as a default flag.


## -returns



On success the HANDLE to the source data is returned; on failure a  <b>NULL</b> value is returned.




## -remarks



The CF_METAFILEPICT, CF_PALETTE, or CF_BITMAP formats receive special handling. They are GDI handles and a new GDI object must be created instead of just copying the bytes. All other formats are duplicated byte-wise.



