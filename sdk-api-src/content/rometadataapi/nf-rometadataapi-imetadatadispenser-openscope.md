---
UID: NF:rometadataapi.IMetaDataDispenser.OpenScope
title: IMetaDataDispenser::OpenScope (rometadataapi.h)
description: Opens an existing, on-disk file and maps its metadata into memory.
helpviewer_keywords: ["IMetaDataDispenser interface [Windows Runtime]","OpenScope method","IMetaDataDispenser.OpenScope","IMetaDataDispenser::OpenScope","OpenScope","OpenScope method [Windows Runtime]","OpenScope method [Windows Runtime]","IMetaDataDispenser interface","rometadataapi/IMetaDataDispenser::OpenScope","winrt.imetadatadispenser_openscope"]
old-location: winrt\imetadatadispenser_openscope.htm
tech.root: WinRT
ms.assetid: 77ba5ee6-082c-478f-83fc-7f6c31ee3c74
ms.date: 12/05/2018
ms.keywords: IMetaDataDispenser interface [Windows Runtime],OpenScope method, IMetaDataDispenser.OpenScope, IMetaDataDispenser::OpenScope, OpenScope, OpenScope method [Windows Runtime], OpenScope method [Windows Runtime],IMetaDataDispenser interface, rometadataapi/IMetaDataDispenser::OpenScope, winrt.imetadatadispenser_openscope
f1_keywords:
- rometadataapi/IMetaDataDispenser.OpenScope
dev_langs:
- c++
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
- IMetaDataDispenser.OpenScope
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMetaDataDispenser::OpenScope


## -description


Opens an existing, on-disk file and maps its metadata into memory.


## -parameters




### -param szScope [in]

The name of the file to be opened. The file must contain common language runtime (CLR) metadata.


### -param dwOpenFlags [in]

Specifies the mode (read, write, and so on) for opening. value of the <a href="https://docs.microsoft.com/dotnet/framework/unmanaged-api/metadata/coropenflags-enumeration">CorOpenFlags</a> enumeration to specify the mode (read, write, and so on) for opening.




### -param riid [in]

The IID of the desired metadata interface to be returned; the caller will use the interface to import (read) or emit (write) metadata.


### -param ppIUnk [out]

The pointer to the returned interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The in-memory copy of the metadata can be queried using methods from one of the "import" interfaces, or added to using methods from the one of the "emit" interfaces.

If the target file does not contain CLR metadata, the <b>OpenScope</b> method will fail.






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatadispenser">IMetaDataDispenser</a>
 

 

