---
UID: NF:imapi2fs.IBootOptions.put_PlatformId
title: IBootOptions::put_PlatformId (imapi2fs.h)
description: Sets the platform identifier that identifies the operating system architecture that the boot image supports.
helpviewer_keywords: ["IBootOptions interface [IMAPI]","put_PlatformId method","IBootOptions.put_PlatformId","IBootOptions::put_PlatformId","imapi.ibootoptions_put_platformid","imapi2fs/IBootOptions::put_PlatformId","put_PlatformId","put_PlatformId method [IMAPI]","put_PlatformId method [IMAPI]","IBootOptions interface"]
old-location: imapi\ibootoptions_put_platformid.htm
tech.root: imapi
ms.assetid: 295f3a3c-0f01-4b9b-b73c-48f075e6a33a
ms.date: 12/05/2018
ms.keywords: IBootOptions interface [IMAPI],put_PlatformId method, IBootOptions.put_PlatformId, IBootOptions::put_PlatformId, imapi.ibootoptions_put_platformid, imapi2fs/IBootOptions::put_PlatformId, put_PlatformId, put_PlatformId method [IMAPI], put_PlatformId method [IMAPI],IBootOptions interface
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
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
 - IBootOptions::put_PlatformId
 - imapi2fs/IBootOptions::put_PlatformId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IBootOptions.put_PlatformId
---

# IBootOptions::put_PlatformId


## -description

Sets the platform identifier that identifies the operating system architecture that the boot image supports.

## -parameters

### -param newVal [in]

Identifies the operating system architecture that the boot image supports. For possible values, see the <a href="/windows/desktop/api/imapi2fs/ne-imapi2fs-platformid">PlatformId</a> enumeration type. The default value is  <b>PlatformX86</b> for Intel x86–based platforms.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions">IBootOptions</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ibootoptions-get_platformid">IBootOptions::get_PlatformId</a>