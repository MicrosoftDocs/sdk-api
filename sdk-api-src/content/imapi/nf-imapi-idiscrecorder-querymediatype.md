---
UID: NF:imapi.IDiscRecorder.QueryMediaType
title: IDiscRecorder::QueryMediaType (imapi.h)
description: Detects the type of media currently inserted in the recorder, if any.
helpviewer_keywords: ["IDiscRecorder interface [IMAPI]","QueryMediaType method","IDiscRecorder.QueryMediaType","IDiscRecorder::QueryMediaType","MEDIA_BLANK","MEDIA_CDDA_CDROM","MEDIA_CD_EXTRA","MEDIA_CD_I","MEDIA_CD_OTHER","MEDIA_CD_ROM_XA","MEDIA_RW","MEDIA_SPECIAL","MEDIA_WRITABLE","QueryMediaType","QueryMediaType method [IMAPI]","QueryMediaType method [IMAPI]","IDiscRecorder interface","_win32_idiscrecorder_querymediatype","base.idiscrecorder_querymediatype","imapi.idiscrecorder_querymediatype","imapi/IDiscRecorder::QueryMediaType"]
old-location: imapi\idiscrecorder_querymediatype.htm
tech.root: imapi
ms.assetid: 40f9376d-5702-4dfb-a69b-0ca4fcfc8d8e
ms.date: 12/05/2018
ms.keywords: IDiscRecorder interface [IMAPI],QueryMediaType method, IDiscRecorder.QueryMediaType, IDiscRecorder::QueryMediaType, MEDIA_BLANK, MEDIA_CDDA_CDROM, MEDIA_CD_EXTRA, MEDIA_CD_I, MEDIA_CD_OTHER, MEDIA_CD_ROM_XA, MEDIA_RW, MEDIA_SPECIAL, MEDIA_WRITABLE, QueryMediaType, QueryMediaType method [IMAPI], QueryMediaType method [IMAPI],IDiscRecorder interface, _win32_idiscrecorder_querymediatype, base.idiscrecorder_querymediatype, imapi.idiscrecorder_querymediatype, imapi/IDiscRecorder::QueryMediaType
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
 - IDiscRecorder::QueryMediaType
 - imapi/IDiscRecorder::QueryMediaType
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
 - IDiscRecorder.QueryMediaType
---

# IDiscRecorder::QueryMediaType


## -description

Detects the type of media currently inserted in the recorder, if any.

## -parameters

### -param fMediaType [out]

If there is no media, both <i>fMediaType</i> and <i>fMediaFlags</i> are zero. If there is media, <i>fMediaType</i> contains one or more of the following values. 



					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MEDIA_CD_EXTRA"></a><a id="media_cd_extra"></a><dl>
<dt><b>MEDIA_CD_EXTRA</b></dt>
</dl>
</td>
<td width="60%">
4

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIA_CD_I"></a><a id="media_cd_i"></a><dl>
<dt><b>MEDIA_CD_I</b></dt>
</dl>
</td>
<td width="60%">
3

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIA_CD_OTHER"></a><a id="media_cd_other"></a><dl>
<dt><b>MEDIA_CD_OTHER</b></dt>
</dl>
</td>
<td width="60%">
5

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIA_CD_ROM_XA"></a><a id="media_cd_rom_xa"></a><dl>
<dt><b>MEDIA_CD_ROM_XA</b></dt>
</dl>
</td>
<td width="60%">
2

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIA_CDDA_CDROM"></a><a id="media_cdda_cdrom"></a><dl>
<dt><b>MEDIA_CDDA_CDROM</b></dt>
</dl>
</td>
<td width="60%">
1

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIA_SPECIAL"></a><a id="media_special"></a><dl>
<dt><b>MEDIA_SPECIAL</b></dt>
</dl>
</td>
<td width="60%">
6

</td>
</tr>
</table>

### -param fMediaFlags [out]

If there is media, this parameter contains one or more of the following values. 



					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MEDIA_BLANK"></a><a id="media_blank"></a><dl>
<dt><b>MEDIA_BLANK</b></dt>
</dl>
</td>
<td width="60%">
0x1

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIA_RW"></a><a id="media_rw"></a><dl>
<dt><b>MEDIA_RW</b></dt>
</dl>
</td>
<td width="60%">
0x2

</td>
</tr>
<tr>
<td width="40%"><a id="MEDIA_WRITABLE"></a><a id="media_writable"></a><dl>
<dt><b>MEDIA_WRITABLE</b></dt>
</dl>
</td>
<td width="60%">
0x4

</td>
</tr>
</table>

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscrecorder">IDiscRecorder</a>