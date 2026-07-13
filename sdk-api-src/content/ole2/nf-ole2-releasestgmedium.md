---
UID: NF:ole2.ReleaseStgMedium
title: ReleaseStgMedium function (ole2.h)
description: Frees the specified storage medium.
helpviewer_keywords: ["ReleaseStgMedium","ReleaseStgMedium function [COM]","_ole_ReleaseStgMedium","com.releasestgmedium","ole2/ReleaseStgMedium"]
old-location: com\releasestgmedium.htm
tech.root: com
ms.assetid: da7d7bcb-0b5b-4053-8f0e-ff311c424375
ms.date: 12/05/2018
ms.keywords: ReleaseStgMedium, ReleaseStgMedium function [COM], _ole_ReleaseStgMedium, com.releasestgmedium, ole2/ReleaseStgMedium
req.header: ole2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ReleaseStgMedium
 - ole2/ReleaseStgMedium
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - Ole32.dll
 - API-MS-Win-OLE32-IE-l1-1-0.dll
 - ole32_wp.dll
 - Ext-MS-Win-Com-Ole32-L1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - ReleaseStgMedium
req.apiset: ext-ms-win-com-ole32-l1-1-3 (introduced in Windows 10, version 10.0.10240)
---

# ReleaseStgMedium function


## -description

Frees the specified storage medium.

## -parameters

### -param LPSTGMEDIUM [in]

Pointer to the storage medium that is to be freed.

## -remarks

The <b>ReleaseStgMedium</b> function calls the appropriate method or function to release the specified storage medium. Use this function during data transfer operations where storage medium structures are parameters, such as <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a> or <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-setdata">IDataObject::SetData</a>. In addition to identifying the type of the storage medium, this structure specifies the appropriate <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method for releasing the storage medium when it is no longer needed.

It is common to pass a <a href="/windows/win32/api/objidl/ns-objidl-ustgmedium-r1">STGMEDIUM</a> from one body of code to another, such as in <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a>, in which the one called can allocate a medium and return it to the caller. <b>ReleaseStgMedium</b> permits flexibility in whether the receiving body of code owns the medium, or whether the original provider of the medium still owns it, in which case the receiving code needs to inform the provider that it can free the medium.

When the original provider of the medium is responsible for freeing the medium, the provider calls <b>ReleaseStgMedium</b>, specifying the medium and the appropriate <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer as the <b>punkForRelease</b> structure member. Depending on the type of storage medium being freed, one of the following actions is taken, followed by a call to the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method on the specified <b>IUnknown</b> pointer.

<table>
<tr>
<th>Medium</th>
<th>ReleaseStgMedium Action</th>
</tr>
<tr>
<td>TYMED_HGLOBAL</td>
<td>None.</td>
</tr>
<tr>
<td>TYMED_GDI</td>
<td>None.</td>
</tr>
<tr>
<td>TYMED_ENHMF</td>
<td>None.</td>
</tr>
<tr>
<td>TYMED_MFPICT</td>
<td>None.</td>
</tr>
<tr>
<td>TYMED_FILE</td>
<td>Frees the file name string using standard memory management mechanisms.</td>
</tr>
<tr>
<td>TYMED_ISTREAM</td>
<td>Calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IStream::Release</a>.</td>
</tr>
<tr>
<td>TYMED_ISTORAGE</td>
<td>Calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IStorage::Release</a>.</td>
</tr>
</table>
 

The provider indicates that the receiver of the medium is responsible for freeing the medium by specifying <b>NULL</b> for the <b>punkForRelease</b> structure member. Then the receiver calls <b>ReleaseStgMedium</b>, which makes a call as described in the following table depending on the type of storage medium being freed.

<table>
<tr>
<th>Medium</th>
<th>ReleaseStgMedium Action</th>
</tr>
<tr>
<td>TYMED_HGLOBAL</td>
<td>Calls the <a href="/windows/desktop/api/winbase/nf-winbase-globalfree">GlobalFree</a> function on the handle.</td>
</tr>
<tr>
<td>TYMED_GDI</td>
<td>Calls the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function on the handle.</td>
</tr>
<tr>
<td>TYMED_ENHMF</td>
<td>Deletes the enhanced metafile.</td>
</tr>
<tr>
<td>TYMED_MFPICT</td>
<td>The hMF that it contains is deleted with the <a href="/windows/desktop/api/wingdi/nf-wingdi-deletemetafile">DeleteMetaFile</a> function; then the handle itself is passed to <a href="/windows/desktop/api/winbase/nf-winbase-globalfree">GlobalFree</a>.</td>
</tr>
<tr>
<td>TYMED_FILE</td>
<td>Frees the disk file by deleting it. Frees the file name string by using the standard memory management mechanisms.</td>
</tr>
<tr>
<td>TYMED_ISTREAM</td>
<td>Calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IStream::Release</a>.</td>
</tr>
<tr>
<td>TYMED_ISTORAGE</td>
<td>Calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IStorage::Release</a>.</td>
</tr>
</table>
 

In either case, after the call to <b>ReleaseStgMedium</b>, the specified storage medium is invalid and can no longer be used.

## -see-also

<a href="/windows/win32/api/objidl/ns-objidl-ustgmedium-r1">STGMEDIUM</a>
