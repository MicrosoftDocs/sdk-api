---
UID: NF:strmif.IDvdInfo2.GetDiscID
title: IDvdInfo2::GetDiscID method
author: windows-driver-content
description: The GetDiscID method retrieves a system-generated 64-bit identification number for the specified DVD.
old-location: dshow\idvdinfo2_getdiscid.htm
old-project: DirectShow
ms.assetid: 53c244ff-026f-4838-b805-316ef3d872d1
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetDiscID method [DirectShow], GetDiscID method [DirectShow], IDvdInfo2 interface, GetDiscID,IDvdInfo2.GetDiscID, IDvdInfo2, IDvdInfo2 interface [DirectShow], GetDiscID method, IDvdInfo2::GetDiscID, IDvdInfo2GetDiscID, dshow.idvdinfo2_getdiscid, strmif/IDvdInfo2::GetDiscID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IDvdInfo2.GetDiscID
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo2::GetDiscID method


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
The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> is not initialized.

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




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2 Interface</a>
 

 

