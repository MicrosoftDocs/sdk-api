---
UID: NF:imapi2fs.IFsiItem.get_LastAccessedTime
title: IFsiItem::get_LastAccessedTime (imapi2fs.h)
description: Retrieves the date and time the directory or file item was last accessed in the file system image.
helpviewer_keywords: ["IFsiItem interface [IMAPI]","get_LastAccessedTime method","IFsiItem.get_LastAccessedTime","IFsiItem::get_LastAccessedTime","get_LastAccessedTime","get_LastAccessedTime method [IMAPI]","get_LastAccessedTime method [IMAPI]","IFsiItem interface","imapi.ifsiitem_get_lastaccessedtime","imapi2fs/IFsiItem::get_LastAccessedTime"]
old-location: imapi\ifsiitem_get_lastaccessedtime.htm
tech.root: imapi
ms.assetid: e12f4c62-2dc8-4155-9cd7-0dea982d7b5a
ms.date: 12/05/2018
ms.keywords: IFsiItem interface [IMAPI],get_LastAccessedTime method, IFsiItem.get_LastAccessedTime, IFsiItem::get_LastAccessedTime, get_LastAccessedTime, get_LastAccessedTime method [IMAPI], get_LastAccessedTime method [IMAPI],IFsiItem interface, imapi.ifsiitem_get_lastaccessedtime, imapi2fs/IFsiItem::get_LastAccessedTime
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
 - IFsiItem::get_LastAccessedTime
 - imapi2fs/IFsiItem::get_LastAccessedTime
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
 - IFsiItem.get_LastAccessedTime
---

# IFsiItem::get_LastAccessedTime


## -description

Retrieves the date and time the directory or file item was last accessed in the file system image.

## -parameters

### -param pVal [out]

Date and time that the item directory or file was last accessed in the file system image, according to UTC time.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

UDFS (UDF) uses the <i>LastAccessedTime</i> value for the <i>CreationTime</i>, as IMAPI does not currently support the <i>CreationTime</i> extended attribute.

CDFS (ISO 9660) sets the <i>LastAccessedTime</i> value retrieved by this method to 0, as only the recording time is stored within the File/Directory descriptor.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem">IFsiItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-put_lastaccessedtime">IFsiItem::put_LastAccessedTime</a>