---
UID: NF:rometadataapi.IMetaDataDispenserEx.GetCORSystemDirectory
title: IMetaDataDispenserEx::GetCORSystemDirectory (rometadataapi.h)
description: Gets the directory that holds the current common language runtime (CLR). This method is supported only for use by out-of-process debuggers. If called from another component, it will return E_NOTIMPL.
helpviewer_keywords: ["GetCORSystemDirectory","GetCORSystemDirectory method [Windows Runtime]","GetCORSystemDirectory method [Windows Runtime]","IMetaDataDispenserEx interface","IMetaDataDispenserEx interface [Windows Runtime]","GetCORSystemDirectory method","IMetaDataDispenserEx.GetCORSystemDirectory","IMetaDataDispenserEx::GetCORSystemDirectory","rometadataapi/IMetaDataDispenserEx::GetCORSystemDirectory","winrt.imetadatadispenserex_getcorsystemdirectory"]
old-location: winrt\imetadatadispenserex_getcorsystemdirectory.htm
tech.root: WinRT
ms.assetid: 4f061c7f-bcb8-4b1e-b84b-0398f08a6d69
ms.date: 12/05/2018
ms.keywords: GetCORSystemDirectory, GetCORSystemDirectory method [Windows Runtime], GetCORSystemDirectory method [Windows Runtime],IMetaDataDispenserEx interface, IMetaDataDispenserEx interface [Windows Runtime],GetCORSystemDirectory method, IMetaDataDispenserEx.GetCORSystemDirectory, IMetaDataDispenserEx::GetCORSystemDirectory, rometadataapi/IMetaDataDispenserEx::GetCORSystemDirectory, winrt.imetadatadispenserex_getcorsystemdirectory
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
 - IMetaDataDispenserEx::GetCORSystemDirectory
 - rometadataapi/IMetaDataDispenserEx::GetCORSystemDirectory
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
 - IMetaDataDispenserEx.GetCORSystemDirectory
---

# IMetaDataDispenserEx::GetCORSystemDirectory


## -description

Gets the directory that holds the current common language runtime (CLR). This method is supported only for use by out-of-process debuggers. If called from another component, it will return E_NOTIMPL.

## -parameters

### -param szBuffer [out]

The buffer to receive the directory name.

### -param cchBuffer [in]

The size, in bytes, of <i>szBuffer</i>.

### -param pchBuffer [out]

The number of bytes actually returned in <i>szBuffer</i>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatadispenserex">IMetaDataDispenserEx</a>