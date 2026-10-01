---
UID: NF:wuapi.IUpdate.get_DeltaCompressedContentAvailable
title: IUpdate::get_DeltaCompressedContentAvailable (wuapi.h)
description: Gets a Boolean value that indicates whether delta-compressed content is available on a server for the update.
helpviewer_keywords: ["DeltaCompressedContentAvailable property [Windows Update Agent]","DeltaCompressedContentAvailable property [Windows Update Agent]","IUpdate interface","IUpdate interface [Windows Update Agent]","DeltaCompressedContentAvailable property","IUpdate.DeltaCompressedContentAvailable","IUpdate.get_DeltaCompressedContentAvailable","IUpdate::DeltaCompressedContentAvailable","IUpdate::get_DeltaCompressedContentAvailable","get_DeltaCompressedContentAvailable","wua.iupdate_deltacompressedcontentavailable","wuapi/IUpdate::DeltaCompressedContentAvailable","wuapi/IUpdate::get_DeltaCompressedContentAvailable"]
old-location: wua\iupdate_deltacompressedcontentavailable.htm
tech.root: wua
ms.assetid: b713a349-45fe-492a-a966-17112edf00ec
ms.date: 12/05/2018
ms.keywords: DeltaCompressedContentAvailable property [Windows Update Agent], DeltaCompressedContentAvailable property [Windows Update Agent],IUpdate interface, IUpdate interface [Windows Update Agent],DeltaCompressedContentAvailable property, IUpdate.DeltaCompressedContentAvailable, IUpdate.get_DeltaCompressedContentAvailable, IUpdate::DeltaCompressedContentAvailable, IUpdate::get_DeltaCompressedContentAvailable, get_DeltaCompressedContentAvailable, wua.iupdate_deltacompressedcontentavailable, wuapi/IUpdate::DeltaCompressedContentAvailable, wuapi/IUpdate::get_DeltaCompressedContentAvailable
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdate::get_DeltaCompressedContentAvailable
 - wuapi/IUpdate::get_DeltaCompressedContentAvailable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdate.DeltaCompressedContentAvailable
 - IUpdate.get_DeltaCompressedContentAvailable
---

# IUpdate::get_DeltaCompressedContentAvailable


## -description

Gets a Boolean value that indicates whether delta-compressed content is available on a server for the update.

This property is read-only.

## -parameters

### -param retval [out, retval]

Type: <b>VARIANT_BOOL*</b>

A pointer to a variable of type <a href="/windows/win32/api/oaidl/ns-oaidl-variant#__variant_name_2__variant_name_3bool">VARIANT_BOOL</a> that receives <b>VARIANT_TRUE</b> if delta-compressed content is available on a server for the update, and <b>VARIANT_FALSE</b> if not.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>