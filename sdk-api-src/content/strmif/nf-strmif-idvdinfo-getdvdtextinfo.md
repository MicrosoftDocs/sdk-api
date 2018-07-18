---
UID: NF:strmif.IDvdInfo.GetDVDTextInfo
title: IDvdInfo::GetDVDTextInfo
author: windows-sdk-content
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the TXTDT_MG structure, which can contain text descriptions for title name, volume name, producer name, vocalist name, and so on, in various languages.
old-location: dshow\idvdinfo_getdvdtextinfo.htm
old-project: DirectShow
ms.assetid: e58fcd07-682a-4c41-9501-d55ba092a150
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetDVDTextInfo, GetDVDTextInfo method [DirectShow], GetDVDTextInfo method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetDVDTextInfo method, IDvdInfo.GetDVDTextInfo, IDvdInfo::GetDVDTextInfo, IDvdInfoGetDVDTextInfo, dshow.idvdinfo_getdvdtextinfo, strmif/IDvdInfo::GetDVDTextInfo
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDvdInfo.GetDVDTextInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo::GetDVDTextInfo


## -description



<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the <b>TXTDT_MG</b> structure, which can contain text descriptions for title name, volume name, producer name, vocalist name, and so on, in various languages.




## -parameters




### -param pTextManager [out]

Pointer to the retrieved text manager.


### -param ulBufSize




### -param pulActualSize






#### - cbBufSize [in]

Size of the buffer for <i>pTextManager</i>, in bytes.


#### - pcbActualSize [out]

Pointer to a value containing the number of bytes of data returned.


## -returns



Returns an <b>HRESULT</b> value .

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

If the supplied buffer size in <i>cbBufSize</i> is too small for the data, (for example if <i>cbBufSize</i> equals zero), then this method returns E_OUTOFMEMORY and sets the value pointed to by <i>pcbActualSize</i> to the required size.

For more information, refer to Section 4.1.6 and Annex A of the DVD-Video specification.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b0c5dfe-aa1b-4ad0-9272-f1351e494b11">IDvdInfo Interface</a>
 

 

