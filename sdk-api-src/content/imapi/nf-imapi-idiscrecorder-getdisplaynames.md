---
UID: NF:imapi.IDiscRecorder.GetDisplayNames
title: IDiscRecorder::GetDisplayNames (imapi.h)
description: Retrieves a formatted name for the recorder that can be displayed. The name consists of the manufacturer and product identifier of the device.
helpviewer_keywords: ["GetDisplayNames","GetDisplayNames method [IMAPI]","GetDisplayNames method [IMAPI]","IDiscRecorder interface","IDiscRecorder interface [IMAPI]","GetDisplayNames method","IDiscRecorder.GetDisplayNames","IDiscRecorder::GetDisplayNames","_win32_idiscrecorder_getdisplaynames","base.idiscrecorder_getdisplaynames","imapi.idiscrecorder_getdisplaynames","imapi/IDiscRecorder::GetDisplayNames"]
old-location: imapi\idiscrecorder_getdisplaynames.htm
tech.root: imapi
ms.assetid: 0f20cae4-3f9c-49bb-9b82-13351b889a31
ms.date: 12/05/2018
ms.keywords: GetDisplayNames, GetDisplayNames method [IMAPI], GetDisplayNames method [IMAPI],IDiscRecorder interface, IDiscRecorder interface [IMAPI],GetDisplayNames method, IDiscRecorder.GetDisplayNames, IDiscRecorder::GetDisplayNames, _win32_idiscrecorder_getdisplaynames, base.idiscrecorder_getdisplaynames, imapi.idiscrecorder_getdisplaynames, imapi/IDiscRecorder::GetDisplayNames
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
 - IDiscRecorder::GetDisplayNames
 - imapi/IDiscRecorder::GetDisplayNames
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
 - IDiscRecorder.GetDisplayNames
---

# IDiscRecorder::GetDisplayNames


## -description

Retrieves a formatted name for the recorder that can be displayed. The name consists of the manufacturer and product identifier of the device.

## -parameters

### -param pbstrVendorID [out]

Vendor of the disc recorder. This parameter can be <b>NULL</b>.

### -param pbstrProductID [out]

Product name of the disc recorder. This parameter can be <b>NULL</b>.

### -param pbstrRevision [out]

Revision of the disc recorder. This is typically the revision of the recorder firmware, but it can be a revision for the entire device. This parameter can be <b>NULL</b>.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

The display names are typically combined into a string that is displayed in recorder selection list boxes or other GUI components.

The combination of these three strings does not produce a unique identifier for this specific recorder. Combine these strings with the string returned from 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscrecorder-getpath">GetPath</a> to create a unique value.

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscrecorder">IDiscRecorder</a>