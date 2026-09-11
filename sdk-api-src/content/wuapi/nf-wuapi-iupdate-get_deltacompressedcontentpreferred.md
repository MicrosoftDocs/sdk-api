---
UID: NF:wuapi.IUpdate.get_DeltaCompressedContentPreferred
title: IUpdate::get_DeltaCompressedContentPreferred (wuapi.h)
description: Gets a Boolean value that indicates whether to prefer delta-compressed content during the download and install or uninstall of the update if delta-compressed content is available.
helpviewer_keywords: ["DeltaCompressedContentPreferred property [Windows Update Agent]","DeltaCompressedContentPreferred property [Windows Update Agent]","IUpdate interface","IUpdate interface [Windows Update Agent]","DeltaCompressedContentPreferred property","IUpdate.DeltaCompressedContentPreferred","IUpdate.get_DeltaCompressedContentPreferred","IUpdate::DeltaCompressedContentPreferred","IUpdate::get_DeltaCompressedContentPreferred","get_DeltaCompressedContentPreferred","wua.iupdate_deltacompressedcontentpreferred","wuapi/IUpdate::DeltaCompressedContentPreferred","wuapi/IUpdate::get_DeltaCompressedContentPreferred"]
old-location: wua\iupdate_deltacompressedcontentpreferred.htm
tech.root: wua
ms.assetid: 9fdb3918-9fc7-491f-9abb-4c2f13528817
ms.date: 12/05/2018
ms.keywords: DeltaCompressedContentPreferred property [Windows Update Agent], DeltaCompressedContentPreferred property [Windows Update Agent],IUpdate interface, IUpdate interface [Windows Update Agent],DeltaCompressedContentPreferred property, IUpdate.DeltaCompressedContentPreferred, IUpdate.get_DeltaCompressedContentPreferred, IUpdate::DeltaCompressedContentPreferred, IUpdate::get_DeltaCompressedContentPreferred, get_DeltaCompressedContentPreferred, wua.iupdate_deltacompressedcontentpreferred, wuapi/IUpdate::DeltaCompressedContentPreferred, wuapi/IUpdate::get_DeltaCompressedContentPreferred
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
 - IUpdate::get_DeltaCompressedContentPreferred
 - wuapi/IUpdate::get_DeltaCompressedContentPreferred
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
 - IUpdate.DeltaCompressedContentPreferred
 - IUpdate.get_DeltaCompressedContentPreferred
---

# IUpdate::get_DeltaCompressedContentPreferred


## -description

 Gets a Boolean value that indicates whether to prefer delta-compressed content during the download and install or uninstall of the update if delta-compressed content is available.

This property is read-only.

## -parameters

### -param retval [out, retval]

Type: <b>VARIANT_BOOL*</b>

A pointer to a variable of type <a href="/windows/win32/api/oaidl/ns-oaidl-variant#__variant_name_2__variant_name_3bool">VARIANT_BOOL</a> that receives <b>VARIANT_TRUE</b> if delta-compressed content is preferred, and <b>VARIANT_FALSE</b> if not.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>