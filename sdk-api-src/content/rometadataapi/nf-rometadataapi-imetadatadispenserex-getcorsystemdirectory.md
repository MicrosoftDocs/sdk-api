---
UID: NF:rometadataapi.IMetaDataDispenserEx.GetCORSystemDirectory
title: IMetaDataDispenserEx::GetCORSystemDirectory
author: windows-sdk-content
description: Gets the directory that holds the current common language runtime (CLR). This method is supported only for use by out-of-process debuggers. If called from another component, it will return E_NOTIMPL.
old-location: winrt\imetadatadispenserex_getcorsystemdirectory.htm
tech.root: WinRT
ms.assetid: 4f061c7f-bcb8-4b1e-b84b-0398f08a6d69
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetCORSystemDirectory, GetCORSystemDirectory method [Windows Runtime], GetCORSystemDirectory method [Windows Runtime],IMetaDataDispenserEx interface, IMetaDataDispenserEx interface [Windows Runtime],GetCORSystemDirectory method, IMetaDataDispenserEx.GetCORSystemDirectory, IMetaDataDispenserEx::GetCORSystemDirectory, rometadataapi/IMetaDataDispenserEx::GetCORSystemDirectory, winrt.imetadatadispenserex_getcorsystemdirectory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataDispenserEx.GetCORSystemDirectory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- rometadataapi.h
: 
- IMetaDataDispenserEx.GetCORSystemDirectory
: 
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b61c8d05-6d73-4f84-95b2-2a892f3de77c">IMetaDataDispenserEx</a>
 

 

