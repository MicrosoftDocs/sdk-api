---
UID: NF:strmif.IDvdInfo.GetPlayerParentalLevel
title: IDvdInfo::GetPlayerParentalLevel
author: windows-sdk-content
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the current parental level and country/region code settings for the DVD player.
old-location: dshow\idvdinfo_getplayerparentallevel.htm
old-project: DirectShow
ms.assetid: 2b4111db-fbb1-4da7-85e1-ddd3f5718225
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetPlayerParentalLevel, GetPlayerParentalLevel method [DirectShow], GetPlayerParentalLevel method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetPlayerParentalLevel method, IDvdInfo.GetPlayerParentalLevel, IDvdInfo::GetPlayerParentalLevel, IDvdInfoGetPlayerParentalLevel, dshow.idvdinfo_getplayerparentallevel, strmif/IDvdInfo::GetPlayerParentalLevel
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmif.h
api_name:
-	IDvdInfo.GetPlayerParentalLevel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo::GetPlayerParentalLevel


## -description



<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the current parental level and country/region code settings for the DVD player.




## -parameters




### -param pulParentalLevel




### -param pulCountryCode






#### - pCountryCode [out]

Pointer to a value indicating the current country/region code.


#### - pParentalLevel [out]

Pointer to a value indicating the current parental level.


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

For the defined parental levels, see Table 3.3.4-1 of the DVD-Video specification.

Valid parental levels are 1 through 8 if parental management is enabled, 0xffffffff if parental management is disabled.

For the country/region codes, see ISO3166 : Alpha-2 Code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b0c5dfe-aa1b-4ad0-9272-f1351e494b11">IDvdInfo Interface</a>
 

 

