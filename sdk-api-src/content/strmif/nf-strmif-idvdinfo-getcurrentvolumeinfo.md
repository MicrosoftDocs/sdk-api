---
UID: NF:strmif.IDvdInfo.GetCurrentVolumeInfo
title: IDvdInfo::GetCurrentVolumeInfo
author: windows-driver-content
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the current DVD volume information.
old-location: dshow\idvdinfo_getcurrentvolumeinfo.htm
old-project: DirectShow
ms.assetid: 2da53db9-5565-4bca-ba0a-90f7e07ccbb9
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: GetCurrentVolumeInfo, GetCurrentVolumeInfo method [DirectShow], GetCurrentVolumeInfo method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetCurrentVolumeInfo method, IDvdInfo.GetCurrentVolumeInfo, IDvdInfo::GetCurrentVolumeInfo, IDvdInfoGetCurrentVolumeInfo, dshow.idvdinfo_getcurrentvolumeinfo, strmif/IDvdInfo::GetCurrentVolumeInfo
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmif.h
api_name:
-	IDvdInfo.GetCurrentVolumeInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo::GetCurrentVolumeInfo


## -description



<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the current DVD volume information.




## -parameters




### -param pulNumOfVol




### -param pulThisVolNum




### -param pSide [out]

Pointer to the retrieved current disc side (<a href="https://msdn.microsoft.com/50ea509c-15fc-4066-ad86-04e5e87fdfa6">DVD_DISC_SIDE</a>).


### -param pulNumOfTitles






#### - pNumOfTitles [out]

Pointer to the retrieved number of titles available in this volume.


#### - pNumOfVol [out]

Pointer to the retrieved number of volumes in the volume set.


#### - pThisVolNum [out]

Pointer to the retrieved volume number for this root directory.


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




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b0c5dfe-aa1b-4ad0-9272-f1351e494b11">IDvdInfo Interface</a>
 

 

