---
UID: NF:imapi.IJolietDiscMaster.GetDataBlockSize
title: IJolietDiscMaster::GetDataBlockSize (imapi.h)
description: Retrieves the size of a data block.
helpviewer_keywords: ["GetDataBlockSize","GetDataBlockSize method [IMAPI]","GetDataBlockSize method [IMAPI]","IJolietDiscMaster interface","IJolietDiscMaster interface [IMAPI]","GetDataBlockSize method","IJolietDiscMaster.GetDataBlockSize","IJolietDiscMaster::GetDataBlockSize","_win32_ijolietdiscmaster_getdatablocksize","base.ijolietdiscmaster_getdatablocksize","imapi.ijolietdiscmaster_getdatablocksize","imapi/IJolietDiscMaster::GetDataBlockSize"]
old-location: imapi\ijolietdiscmaster_getdatablocksize.htm
tech.root: imapi
ms.assetid: 84bb0330-770d-44ab-8829-e81616f7c805
ms.date: 12/05/2018
ms.keywords: GetDataBlockSize, GetDataBlockSize method [IMAPI], GetDataBlockSize method [IMAPI],IJolietDiscMaster interface, IJolietDiscMaster interface [IMAPI],GetDataBlockSize method, IJolietDiscMaster.GetDataBlockSize, IJolietDiscMaster::GetDataBlockSize, _win32_ijolietdiscmaster_getdatablocksize, base.ijolietdiscmaster_getdatablocksize, imapi.ijolietdiscmaster_getdatablocksize, imapi/IJolietDiscMaster::GetDataBlockSize
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IJolietDiscMaster::GetDataBlockSize
 - imapi/IJolietDiscMaster::GetDataBlockSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IJolietDiscMaster.GetDataBlockSize
---

# IJolietDiscMaster::GetDataBlockSize


## -description

Retrieves the size of a data block.

## -parameters

### -param pnBlockBytes [out]

Total size of a single data block, in bytes.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

This method returns 2048.

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-ijolietdiscmaster">IJolietDiscMaster</a>