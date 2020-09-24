---
UID: NF:imapi.IRedbookDiscMaster.GetAudioBlockSize
title: IRedbookDiscMaster::GetAudioBlockSize (imapi.h)
description: Retrieves the size, in bytes, of an audio block.
helpviewer_keywords: ["GetAudioBlockSize","GetAudioBlockSize method [IMAPI]","GetAudioBlockSize method [IMAPI]","IRedbookDiscMaster interface","IRedbookDiscMaster interface [IMAPI]","GetAudioBlockSize method","IRedbookDiscMaster.GetAudioBlockSize","IRedbookDiscMaster::GetAudioBlockSize","_win32_iredbookdiscmaster_getaudioblocksize","base.iredbookdiscmaster_getaudioblocksize","imapi.iredbookdiscmaster_getaudioblocksize","imapi/IRedbookDiscMaster::GetAudioBlockSize"]
old-location: imapi\iredbookdiscmaster_getaudioblocksize.htm
tech.root: imapi
ms.assetid: 25e8fd75-7a24-421f-b61e-b131dfbbcc8c
ms.date: 12/05/2018
ms.keywords: GetAudioBlockSize, GetAudioBlockSize method [IMAPI], GetAudioBlockSize method [IMAPI],IRedbookDiscMaster interface, IRedbookDiscMaster interface [IMAPI],GetAudioBlockSize method, IRedbookDiscMaster.GetAudioBlockSize, IRedbookDiscMaster::GetAudioBlockSize, _win32_iredbookdiscmaster_getaudioblocksize, base.iredbookdiscmaster_getaudioblocksize, imapi.iredbookdiscmaster_getaudioblocksize, imapi/IRedbookDiscMaster::GetAudioBlockSize
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
 - IRedbookDiscMaster::GetAudioBlockSize
 - imapi/IRedbookDiscMaster::GetAudioBlockSize
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
 - IRedbookDiscMaster.GetAudioBlockSize
---

# IRedbookDiscMaster::GetAudioBlockSize


## -description

Retrieves the size, in bytes, of an audio block.

## -parameters

### -param pnBlockBytes [out]

Total size, in bytes, of a single audio block.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

This method returns 2352.

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-iredbookdiscmaster">IRedbookDiscMaster</a>