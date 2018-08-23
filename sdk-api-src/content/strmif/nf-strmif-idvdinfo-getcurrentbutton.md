---
UID: NF:strmif.IDvdInfo.GetCurrentButton
title: IDvdInfo::GetCurrentButton
author: windows-sdk-content
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the number of available buttons and the currently selected button number.
old-location: dshow\idvdinfo_getcurrentbutton.htm
old-project: DirectShow
ms.assetid: 13df79ea-81c9-4060-8e11-ad7a24a7b5fa
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetCurrentButton, GetCurrentButton method [DirectShow], GetCurrentButton method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetCurrentButton method, IDvdInfo.GetCurrentButton, IDvdInfo::GetCurrentButton, IDvdInfoGetCurrentButton, dshow.idvdinfo_getcurrentbutton, strmif/IDvdInfo::GetCurrentButton
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
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
 - IDvdInfo.GetCurrentButton
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo::GetCurrentButton


## -description



<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the number of available buttons and the currently selected button number.




## -parameters




### -param pulButtonsAvailable




### -param pulCurrentButton






#### - pnButtonsAvailable [out]

Pointer to the number of buttons available.


#### - pnCurrentButton [out]

Pointer to the number of the current button.


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



If buttons are not present this method returns zero for both <i>pnButtonsAvailable</i> and <i>pnCurrentButton</i>.

This method is valid in any domain. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b0c5dfe-aa1b-4ad0-9272-f1351e494b11">IDvdInfo Interface</a>
 

 

