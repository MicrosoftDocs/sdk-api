---
UID: NF:strmif.IDvdInfo.GetTitleAttributes
title: IDvdInfo::GetTitleAttributes
author: windows-sdk-content
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves attributes of all video, audio, and subpicture streams for the specified title, including menus.
old-location: dshow\idvdinfo_gettitleattributes.htm
tech.root: DirectShow
ms.assetid: 012e3860-dfa2-45e8-ab37-2a3a4b2f7f9d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTitleAttributes, GetTitleAttributes method [DirectShow], GetTitleAttributes method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetTitleAttributes method, IDvdInfo.GetTitleAttributes, IDvdInfo::GetTitleAttributes, IDvdInfoGetTitleAttributes, dshow.idvdinfo_gettitleattributes, strmif/IDvdInfo::GetTitleAttributes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDvdInfo.GetTitleAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdInfo::GetTitleAttributes


## -description



<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves attributes of all video, audio, and subpicture streams for the specified title, including menus.




## -parameters




### -param ulTitle [in]

Requested title number. Specify 0xFFFFFFFF for the current title.


### -param pATR [out]

Pointer to the retrieved attributes structure.


## -returns



Returns an <b>HRESULT</b> value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
DVD is not initialized or domain is not DVD_DOMAIN_Title.

</td>
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
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
Requested action is not supported on this domain (<a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
Requested action cannot occur at this point in the movie due to the authoring of the current DVD-Video disc.

</td>
</tr>
</table>
 




## -remarks



This method is valid in any domain. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b0c5dfe-aa1b-4ad0-9272-f1351e494b11">IDvdInfo Interface</a>
 

 

