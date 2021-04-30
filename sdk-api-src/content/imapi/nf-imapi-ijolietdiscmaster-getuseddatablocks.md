---
UID: NF:imapi.IJolietDiscMaster.GetUsedDataBlocks
title: IJolietDiscMaster::GetUsedDataBlocks (imapi.h)
description: Retrieves the total number of data blocks that are in use.
helpviewer_keywords: ["GetUsedDataBlocks","GetUsedDataBlocks method [IMAPI]","GetUsedDataBlocks method [IMAPI]","IJolietDiscMaster interface","IJolietDiscMaster interface [IMAPI]","GetUsedDataBlocks method","IJolietDiscMaster.GetUsedDataBlocks","IJolietDiscMaster::GetUsedDataBlocks","_win32_ijolietdiscmaster_getuseddatablocks","base.ijolietdiscmaster_getuseddatablocks","imapi.ijolietdiscmaster_getuseddatablocks","imapi/IJolietDiscMaster::GetUsedDataBlocks"]
old-location: imapi\ijolietdiscmaster_getuseddatablocks.htm
tech.root: imapi
ms.assetid: 01bde64a-3d91-4830-bd93-f3fe6b109264
ms.date: 12/05/2018
ms.keywords: GetUsedDataBlocks, GetUsedDataBlocks method [IMAPI], GetUsedDataBlocks method [IMAPI],IJolietDiscMaster interface, IJolietDiscMaster interface [IMAPI],GetUsedDataBlocks method, IJolietDiscMaster.GetUsedDataBlocks, IJolietDiscMaster::GetUsedDataBlocks, _win32_ijolietdiscmaster_getuseddatablocks, base.ijolietdiscmaster_getuseddatablocks, imapi.ijolietdiscmaster_getuseddatablocks, imapi/IJolietDiscMaster::GetUsedDataBlocks
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
 - IJolietDiscMaster::GetUsedDataBlocks
 - imapi/IJolietDiscMaster::GetUsedDataBlocks
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
 - IJolietDiscMaster.GetUsedDataBlocks
---

# IJolietDiscMaster::GetUsedDataBlocks


## -description

Retrieves the total number of data blocks that are in use. The data returned from this method is valid only after a 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-setactivediscrecorder">SetActiveDiscRecorder</a> call, especially in a multi-session burn.

## -parameters

### -param pnBlocks [out]

Total number of data blocks in use in the staged image.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-ijolietdiscmaster">IJolietDiscMaster</a>