---
UID: NF:imapi2fs.IFsiFileItem2.get_IsRealTime
title: IFsiFileItem2::get_IsRealTime (imapi2fs.h)
description: Retrieves the property value that specifies if a file item in the file system image is a 'Real-Time' or standard file.
helpviewer_keywords: ["IFsiFileItem2 interface [IMAPI]","get_IsRealTime method","IFsiFileItem2.get_IsRealTime","IFsiFileItem2::get_IsRealTime","get_IsRealTime","get_IsRealTime method [IMAPI]","get_IsRealTime method [IMAPI]","IFsiFileItem2 interface","imapi.ifsifileitem2_get_isrealtime","imapi2fs/IFsiFileItem2::get_IsRealTime"]
old-location: imapi\ifsifileitem2_get_isrealtime.htm
tech.root: imapi
ms.assetid: a8b8fca4-f24c-4698-b84d-7b79ad81d467
ms.date: 12/05/2018
ms.keywords: IFsiFileItem2 interface [IMAPI],get_IsRealTime method, IFsiFileItem2.get_IsRealTime, IFsiFileItem2::get_IsRealTime, get_IsRealTime, get_IsRealTime method [IMAPI], get_IsRealTime method [IMAPI],IFsiFileItem2 interface, imapi.ifsifileitem2_get_isrealtime, imapi2fs/IFsiFileItem2::get_IsRealTime
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - IFsiFileItem2::get_IsRealTime
 - imapi2fs/IFsiFileItem2::get_IsRealTime
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
 - IFsiFileItem2.get_IsRealTime
---

# IFsiFileItem2::get_IsRealTime


## -description

Retrieves the property value that specifies if a file item in the file system image is a 'Real-Time' or standard file.

## -parameters

### -param pVal [out]

Pointer to a value that indicates if the Real-Time attribute of the file is set in the file system image.  A value of <b>VARIANT_TRUE</b> indicates the attribute is set; otherwise, <b>VARIANT_FALSE</b>.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
<dt>Value: 0x80004003</dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_PROPERTY_NOT_ACCESSIBLE</b></dt>
<dt>Value: 0xC0AAB160L</dt>
</dl>
</td>
<td width="60%">
Property '<i>%1!ls!</i>' is not accessible.

</td>
</tr>
</table>

## -remarks

If this method is invoked for a file item representing a named stream, this method returns error code <b>IMAPI_E_PROPERTY_NOT_ACCESSIBLE</b> as
named streams do not have the Real-Time attribute.

The user must enable UDF and set the UDF revision to 2.01 or higher to support Real-Time files.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2">IFsiFileItem2</a>