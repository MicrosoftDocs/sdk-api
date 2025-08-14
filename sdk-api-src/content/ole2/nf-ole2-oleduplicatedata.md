---
UID: NF:ole2.OleDuplicateData
title: OleDuplicateData function (ole2.h)
description: Duplicates the data found in the specified handle and returns a handle to the duplicated data. The source data is in a clipboard format. Use this function to help implement some of the data transfer interfaces such as IDataObject.
helpviewer_keywords: ["OleDuplicateData","OleDuplicateData function [COM]","_ole_OleDuplicateData","com.oleduplicatedata","ole2/OleDuplicateData"]
old-location: com\oleduplicatedata.htm
tech.root: com
ms.assetid: c4ba0b54-e9e1-4c05-b4f8-ce5390cada17
ms.date: 12/05/2018
ms.keywords: OleDuplicateData, OleDuplicateData function [COM], _ole_OleDuplicateData, com.oleduplicatedata, ole2/OleDuplicateData
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleDuplicateData
 - ole2/OleDuplicateData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ole32-misc-l1-1-0.dll
 - Ole32.dll
api_name:
 - OleDuplicateData
---

# OleDuplicateData function


## -description

Duplicates the data found in the specified handle and returns a handle to the duplicated data. The source data is in a clipboard format. Use this function to help implement some of the data transfer interfaces such as <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>.

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