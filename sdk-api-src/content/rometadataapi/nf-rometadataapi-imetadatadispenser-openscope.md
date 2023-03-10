---
UID: NF:rometadataapi.IMetaDataDispenser.OpenScope
title: IMetaDataDispenser::OpenScope (rometadataapi.h)
description: Opens an existing file from disk, and maps its metadata into memory for reading.
helpviewer_keywords: ["IMetaDataDispenser interface [Windows Runtime]","OpenScope method","IMetaDataDispenser.OpenScope","IMetaDataDispenser::OpenScope","OpenScope","OpenScope method [Windows Runtime]","OpenScope method [Windows Runtime]","IMetaDataDispenser interface","rometadataapi/IMetaDataDispenser::OpenScope","winrt.imetadatadispenser_openscope"]
old-location: winrt\imetadatadispenser_openscope.htm
tech.root: WinRT
ms.assetid: 77ba5ee6-082c-478f-83fc-7f6c31ee3c74
ms.date: 12/05/2018
ms.keywords: IMetaDataDispenser interface [Windows Runtime],OpenScope method, IMetaDataDispenser.OpenScope, IMetaDataDispenser::OpenScope, OpenScope, OpenScope method [Windows Runtime], OpenScope method [Windows Runtime],IMetaDataDispenser interface, rometadataapi/IMetaDataDispenser::OpenScope, winrt.imetadatadispenser_openscope
req.header: rometadataapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
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
 - IMetaDataDispenser::OpenScope
 - rometadataapi/IMetaDataDispenser::OpenScope
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataDispenser.OpenScope
---

## -description

Opens an existing file from disk, and maps its metadata into memory for importing (reading).

## -parameters

### -param szScope [in]

The name of the file to be opened. The file must contain common language runtime (CLR) metadata.

### -param dwOpenFlags  [in]

Specifies the mode (read, and so on) for opening. This is a value of the <a href="/dotnet/framework/unmanaged-api/metadata/coropenflags-enumeration">CorOpenFlags</a> enumeration. You can only import (read) from the file, not emit (write) to it.

### -param riid [in]

The IID of the desired metadata interface to be returned; the caller will use the interface to import (read) metadata.

Valid values for *riid* include **IID_IUnknown**, **IID_IMetaDataImport**, **IID_IMetaDataImport2**, **IID_IMetaDataAssemblyImport**, **IID_IMetaDataTables**, and **IID_IMetaDataTables2**.

### -param ppIUnk [out]

The pointer to the returned interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The in-memory copy of the metadata can be queried using methods from one of the "import" interfaces. If the target file doesn't contain CLR metadata, then the <b>OpenScope</b> method will fail.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatadispenser">IMetaDataDispenser</a>
