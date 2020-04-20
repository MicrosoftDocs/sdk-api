---
UID: NF:strmif.IDvdInfo2.GetDiscID
title: IDvdInfo2::GetDiscID (strmif.h)
description: The GetDiscID method retrieves a system-generated 64-bit identification number for the specified DVD.helpviewer_keywords: ["GetDiscID","GetDiscID method [DirectShow]","GetDiscID method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetDiscID method","IDvdInfo2.GetDiscID","IDvdInfo2::GetDiscID","IDvdInfo2GetDiscID","dshow.idvdinfo2_getdiscid","strmif/IDvdInfo2::GetDiscID"]
old-location: dshow\idvdinfo2_getdiscid.htm
tech.root: DirectShow
ms.assetid: 53c244ff-026f-4838-b805-316ef3d872d1
ms.date: 12/05/2018
ms.keywords: GetDiscID, GetDiscID method [DirectShow], GetDiscID method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetDiscID method, IDvdInfo2.GetDiscID, IDvdInfo2::GetDiscID, IDvdInfo2GetDiscID, dshow.idvdinfo2_getdiscid, strmif/IDvdInfo2::GetDiscID
f1_keywords:
- strmif/IDvdInfo2.GetDiscID
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IDvdInfo2.GetDiscID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdInfo2::GetDiscID


## -description



The <code>GetDiscID</code> method retrieves a system-generated 64-bit identification number for the specified DVD.




## -parameters




### -param pszwPath [in]

Path of the volume to use for the disc ID. Specify <b>NULL</b> to use the current or default DVD volume.


### -param pullDiscID [out]

Receives the 64-bit disc ID.


## -returns



Returns one of the following <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> is not initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALID_DISC</b></dt>
</dl>
</td>
<td width="60%">
The specified path is not a valid DVD disc.

</td>
</tr>
</table>
 




## -remarks



The DVD Navigator calculates an identifier ID based on file sizes, dates, and other information, and not the BCA (burst cutting area) value. This number is guaranteed to be the same each time the disc is played. The ID applies to all replicated copies of a disc. In other words, all copies of a specific movie will have the same ID. The odds that two separate titles will have the same ID is sufficiently remote that this ID can be considered "unique" for all practical purposes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>
 

 

