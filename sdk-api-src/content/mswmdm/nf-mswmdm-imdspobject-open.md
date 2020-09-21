---
UID: NF:mswmdm.IMDSPObject.Open
title: IMDSPObject::Open (mswmdm.h)
description: The Open method opens the associated object and prepares it for Read or Write operations. This operation is valid only if the storage object represents a file.
helpviewer_keywords: ["IMDSPObject interface [windows Media Device Manager]","Open method","IMDSPObject.Open","IMDSPObject::Open","IMDSPObjectOpen","Open","Open method [windows Media Device Manager]","Open method [windows Media Device Manager]","IMDSPObject interface","mswmdm/IMDSPObject::Open","wmdm.imdspobject_open"]
old-location: wmdm\imdspobject_open.htm
tech.root: WMDM
ms.assetid: 9e54bcbd-4f14-49e0-8211-2f79f024c80a
ms.date: 12/05/2018
ms.keywords: IMDSPObject interface [windows Media Device Manager],Open method, IMDSPObject.Open, IMDSPObject::Open, IMDSPObjectOpen, Open, Open method [windows Media Device Manager], Open method [windows Media Device Manager],IMDSPObject interface, mswmdm/IMDSPObject::Open, wmdm.imdspobject_open
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMDSPObject::Open
 - mswmdm/IMDSPObject::Open
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPObject.Open
---

# IMDSPObject::Open


## -description

The <b>Open</b> method opens the associated object and prepares it for <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read">Read</a> or <a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write">Write</a> operations. This operation is valid only if the storage object represents a file.

## -parameters

### -param fuMode [in]

Mode in which the file must be opened. It must be one of the following two values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>MDSP_READ</td>
<td>Query whether a subsequent call to <b>Read</b> would be allowed.</td>
</tr>
<tr>
<td>MDSP_WRITE</td>
<td>Query whether a subsequent call to <b>Insert</b> would be allowed.</td>
</tr>
</table>

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

If the underlying file-system does not support opening of multiple files at the same time, the service provider should gracefully the return Win32 error code ERROR_TOO_MANY_OPEN_FILES, if the client attempts to open more than one file at a time.

This method must be implemented. It must not return WMDM_E_NOTSUPPORTED or E_NOTIMPL. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject">IMDSPObject Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-close">IMDSPObject::Close</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read">IMDSPObject::Read</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-seek">IMDSPObject::Seek</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write">IMDSPObject::Write</a>