---
UID: NF:strmif.IDvdInfo.GetCurrentDomain
title: IDvdInfo::GetCurrentDomain
author: windows-sdk-content
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the current DVD domain of the DVD player.
old-location: dshow\idvdinfo_getcurrentdomain.htm
tech.root: DirectShow
ms.assetid: 35f173d5-fb8f-47e2-ab32-87fdb197710a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCurrentDomain, GetCurrentDomain method [DirectShow], GetCurrentDomain method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetCurrentDomain method, IDvdInfo.GetCurrentDomain, IDvdInfo::GetCurrentDomain, IDvdInfoGetCurrentDomain, dshow.idvdinfo_getcurrentdomain, strmif/IDvdInfo::GetCurrentDomain
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
 - IDvdInfo.GetCurrentDomain
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdInfo::GetCurrentDomain


## -description



<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the current DVD domain of the DVD player.




## -parameters




### -param pDomain [out]

Pointer to the current domain that is a member of the <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a> enumerated type.


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
 

 

