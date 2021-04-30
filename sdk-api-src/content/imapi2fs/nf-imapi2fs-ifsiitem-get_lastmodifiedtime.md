---
UID: NF:imapi2fs.IFsiItem.get_LastModifiedTime
title: IFsiItem::get_LastModifiedTime (imapi2fs.h)
description: Retrieves the date and time that the directory or file item was last modified in the file system image.
helpviewer_keywords: ["IFsiItem interface [IMAPI]","get_LastModifiedTime method","IFsiItem.get_LastModifiedTime","IFsiItem::get_LastModifiedTime","get_LastModifiedTime","get_LastModifiedTime method [IMAPI]","get_LastModifiedTime method [IMAPI]","IFsiItem interface","imapi.ifsiitem_get_lastmodifiedtime","imapi2fs/IFsiItem::get_LastModifiedTime"]
old-location: imapi\ifsiitem_get_lastmodifiedtime.htm
tech.root: imapi
ms.assetid: ec7a3b44-817c-4420-81d5-61905aa4f2cf
ms.date: 12/05/2018
ms.keywords: IFsiItem interface [IMAPI],get_LastModifiedTime method, IFsiItem.get_LastModifiedTime, IFsiItem::get_LastModifiedTime, get_LastModifiedTime, get_LastModifiedTime method [IMAPI], get_LastModifiedTime method [IMAPI],IFsiItem interface, imapi.ifsiitem_get_lastmodifiedtime, imapi2fs/IFsiItem::get_LastModifiedTime
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
 - IFsiItem::get_LastModifiedTime
 - imapi2fs/IFsiItem::get_LastModifiedTime
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
 - IFsiItem.get_LastModifiedTime
---

# IFsiItem::get_LastModifiedTime


## -description

Retrieves the date and time that the directory or file item was last modified in the file system image.

## -parameters

### -param pVal [out]

Date and time that the directory or file  item was last modified in the file system image, according to UTC time.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

When implementing this method, a few things should be taken into consideration:

UDFS (UDF) will use the value provided by <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-put_lastmodifiedtime">IFsiItem::put_LastModifiedTime</a> as both the <i>CreationTime</i> and <i>LastModifiedTime</i>.

CDFS (ISO 9660) uses the date/time of recording as the <i>CreationTime</i> and <i>LastModifiedTime</i>. As a result, CDFS sets the value of <i>LastModifiedTime</i> to 0.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem">IFsiItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-put_lastmodifiedtime">IFsiItem::put_LastModifiedTime</a>