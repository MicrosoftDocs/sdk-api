---
UID: NF:rometadataapi.IMetaDataDispenser.OpenScopeOnMemory
title: IMetaDataDispenser::OpenScopeOnMemory (rometadataapi.h)
description: Opens an area of memory that contains existing metadata. That is, this method opens a specified area of memory in which the existing data is treated as metadata.
helpviewer_keywords: ["IMetaDataDispenser interface [Windows Runtime]","OpenScopeOnMemory method","IMetaDataDispenser.OpenScopeOnMemory","IMetaDataDispenser::OpenScopeOnMemory","OpenScopeOnMemory","OpenScopeOnMemory method [Windows Runtime]","OpenScopeOnMemory method [Windows Runtime]","IMetaDataDispenser interface","rometadataapi/IMetaDataDispenser::OpenScopeOnMemory","winrt.imetadatadispenser_openscopeonmemory"]
old-location: winrt\imetadatadispenser_openscopeonmemory.htm
tech.root: WinRT
ms.assetid: 4558b229-0fe9-4ff7-a666-e69b47cb8170
ms.date: 12/05/2018
ms.keywords: IMetaDataDispenser interface [Windows Runtime],OpenScopeOnMemory method, IMetaDataDispenser.OpenScopeOnMemory, IMetaDataDispenser::OpenScopeOnMemory, OpenScopeOnMemory, OpenScopeOnMemory method [Windows Runtime], OpenScopeOnMemory method [Windows Runtime],IMetaDataDispenser interface, rometadataapi/IMetaDataDispenser::OpenScopeOnMemory, winrt.imetadatadispenser_openscopeonmemory
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
 - IMetaDataDispenser::OpenScopeOnMemory
 - rometadataapi/IMetaDataDispenser::OpenScopeOnMemory
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
 - IMetaDataDispenser.OpenScopeOnMemory
---

# IMetaDataDispenser::OpenScopeOnMemory


## -description

Opens an area of memory that contains existing metadata. That is, this method opens a specified area of memory in which the existing data is treated as metadata.

## -parameters

### -param pData [in]

A pointer that specifies the starting address of the memory area.

### -param cbData [in]

The size of the memory area, in bytes.

### -param dwOpenFlags [in]

A value of the <a href="/dotnet/framework/unmanaged-api/metadata/coropenflags-enumeration">CorOpenFlags</a> enumeration to specify the mode (read, write, and so on) for opening.

### -param riid [in]

The IID of the desired metadata interface to be returned; the caller will use the interface to import (read) or emit (write) metadata.

The value of riid must specify one of the "import" or "emit" interfaces. Valid values are <b>IID_IMetaDataEmit</b>, <b>IID_IMetaDataImport</b>, <b>IID_IMetaDataAssemblyEmit</b>, <b>IID_IMetaDataAssemblyImport</b>, <b>IID_IMetaDataEmit2</b>, or <b>IID_IMetaDataImport2</b>.

### -param ppIUnk [out]

The pointer to the returned interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The in-memory copy of the metadata can be queried using methods from one of the "import" interfaces, or added to using methods from the one of the "emit" interfaces.

The <b>OpenScopeOnMemory</b>  method is similar to the <a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatadispenser-openscope">OpenScope</a> method, except that the metadata of interest already exists in memory, rather than in a file on disk.

If the target area of memory does not contain common language runtime (CLR) metadata, the <b>OpenScopeOnMemory</b> method will fail.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatadispenser">IMetaDataDispenser</a>