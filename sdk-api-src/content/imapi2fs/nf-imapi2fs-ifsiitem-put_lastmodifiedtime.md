---
UID: NF:imapi2fs.IFsiItem.put_LastModifiedTime
title: IFsiItem::put_LastModifiedTime (imapi2fs.h)
description: Sets the date and time that the item was last modified in the file system image.
helpviewer_keywords: ["IFsiItem interface [IMAPI]","put_LastModifiedTime method","IFsiItem.put_LastModifiedTime","IFsiItem::put_LastModifiedTime","imapi.ifsiitem_put_lastmodifiedtime","imapi2fs/IFsiItem::put_LastModifiedTime","put_LastModifiedTime","put_LastModifiedTime method [IMAPI]","put_LastModifiedTime method [IMAPI]","IFsiItem interface"]
old-location: imapi\ifsiitem_put_lastmodifiedtime.htm
tech.root: imapi
ms.assetid: 11491b16-0bdc-41a6-a99d-0543cdc3bb64
ms.date: 12/05/2018
ms.keywords: IFsiItem interface [IMAPI],put_LastModifiedTime method, IFsiItem.put_LastModifiedTime, IFsiItem::put_LastModifiedTime, imapi.ifsiitem_put_lastmodifiedtime, imapi2fs/IFsiItem::put_LastModifiedTime, put_LastModifiedTime, put_LastModifiedTime method [IMAPI], put_LastModifiedTime method [IMAPI],IFsiItem interface
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
 - IFsiItem::put_LastModifiedTime
 - imapi2fs/IFsiItem::put_LastModifiedTime
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
 - IFsiItem.put_LastModifiedTime
---

# IFsiItem::put_LastModifiedTime


## -description

Sets the date and time that the item was last modified in the file system image.

## -parameters

### -param newVal [in]

Date and time that the directory or file item was last modified in the file system image, according to UTC time.  Defaults to the time the item was added to the image.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_READONLY</b></dt>
</dl>
</td>
<td width="60%">
FileSystemImage object is in read only mode.

Value: 0xC0AAB102

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate necessary memory.

Value: 0x8007000E

</td>
</tr>
</table>

## -remarks

The last modified time is propagated to the attribute  that users see when viewing the properties of a directory or a file.

When implementing this method, a few things should be taken into consideration:

UDFS (UDF) will use the value provided by <b>IFsiItem::put_LastModifiedTime</b> as both the <i>CreationTime</i> and <i>LastModifiedTime</i>.

CDFS (ISO 9660) uses the date/time of recording as the <i>CreationTime</i> and <i>LastModifiedTime</i>. As a result, CDFS sets the value of <i>LastModifiedTime</i> to 0.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem">IFsiItem</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsiitem-get_lastmodifiedtime">IFsiItem::get_LastModifiedTime</a>