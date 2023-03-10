---
UID: NF:imapi2fs.IFsiFileItem2.put_IsRealTime
title: IFsiFileItem2::put_IsRealTime (imapi2fs.h)
description: Sets the 'Real-Time' attribute of a file in a file system. This attribute specifies whether or not the content requires a minimum data-transfer rate when writing or reading, for example, audio and video data.
helpviewer_keywords: ["IFsiFileItem2 interface [IMAPI]","put_IsRealTime method","IFsiFileItem2.put_IsRealTime","IFsiFileItem2::put_IsRealTime","imapi.ifsifileitem2_put_isrealtime","imapi2fs/IFsiFileItem2::put_IsRealTime","put_IsRealTime","put_IsRealTime method [IMAPI]","put_IsRealTime method [IMAPI]","IFsiFileItem2 interface"]
old-location: imapi\ifsifileitem2_put_isrealtime.htm
tech.root: imapi
ms.assetid: 69ec720a-67b3-4cd7-b291-feb303ab1803
ms.date: 12/05/2018
ms.keywords: IFsiFileItem2 interface [IMAPI],put_IsRealTime method, IFsiFileItem2.put_IsRealTime, IFsiFileItem2::put_IsRealTime, imapi.ifsifileitem2_put_isrealtime, imapi2fs/IFsiFileItem2::put_IsRealTime, put_IsRealTime, put_IsRealTime method [IMAPI], put_IsRealTime method [IMAPI],IFsiFileItem2 interface
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
 - IFsiFileItem2::put_IsRealTime
 - imapi2fs/IFsiFileItem2::put_IsRealTime
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
 - IFsiFileItem2.put_IsRealTime
---

# IFsiFileItem2::put_IsRealTime


## -description

Sets the 'Real-Time' attribute of a file in a file system. This attribute specifies whether or not the content requires a minimum data-transfer rate when writing or reading, for example, audio and video data.

## -parameters

### -param newVal [in]

Specify <b>VARIANT_TRUE</b> to set the Real-Time attribute of a file in the file system image; otherwise, <b>VARIANT_FALSE</b>. The default is <b>VARIANT_FALSE</b>.

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
<dt><b>IMAPI_S_IMAGE_FEATURE_NOT_SUPPORTED</b></dt>
<dt>Value: 0x00AAB15FL</dt>
</dl>
</td>
<td width="60%">
Feature is not supported for the current file system revision, and as a result, the file has been marked as Real-Time but will not appear as such in the resultant file system image unless UDF revision 2.01 or higher is enabled in the file system object.

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
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_INVALID_PARAM</b></dt>
<dt>Value: 0xC0AAB101</dt>
</dl>
</td>
<td width="60%">
The value specified for parameter '<i>%1!ls!</i>' is invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Currently, S_OK is returned when using this method to set a  Real-Time attribute   value of a file that is 'Read Only' as a result of a successful  <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage">CreateResultImage</a> operation.</div>
<div> </div>

## -remarks

The <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree">IFsiDirectoryItem::AddTree</a> and <a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem2-addtreewithnamedstreams">IFsiDirectoryItem2::AddTreeWithNamedStreams</a> methods do not set the Real-Time attribute while adding files to a file system image. To mark files  as Real-time files, they must be enumerated after they have been added to the file system image and have the Real-Time attribute set individually.
 
 

If this method is invoked for a file item representing a named stream, this method returns error code <b>IMAPI_E_PROPERTY_NOT_ACCESSIBLE</b> as
named streams do not have the Real-Time attribute.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2">IFsiFileItem2</a>