---
UID: NF:strmif.IDvdControl.ParentalLevelSelect
title: IDvdControl::ParentalLevelSelect
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Sets the parental access level for the current media file.
old-location: dshow\idvdcontrol_parentallevelselect.htm
old-project: DirectShow
ms.assetid: ca572d89-b188-442d-884f-0cffa71c2892
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IDvdControl interface [DirectShow],ParentalLevelSelect method, IDvdControl.ParentalLevelSelect, IDvdControl::ParentalLevelSelect, IDvdControlParentalLevelSelect, ParentalLevelSelect, ParentalLevelSelect method [DirectShow], ParentalLevelSelect method [DirectShow],IDvdControl interface, dshow.idvdcontrol_parentallevelselect, strmif/IDvdControl::ParentalLevelSelect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Reference:\_Dshowh
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
 - Quartz.dll
api_name:
 - IDvdControl.ParentalLevelSelect
product: Windows
targetos: Windows
req.lib: 
req.dll: Quartz.dll
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl::ParentalLevelSelect


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Sets the parental access level for the current media file.




## -parameters




### -param ulParentalLevel

Value that specifies the current media file parental access level. Should be a value from 1 to 8, inclusive. Predefined parental levels are as follows:

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>1</td>
<td>The rating is G, General.</td>
</tr>
<tr>
<td>3</td>
<td>The rating is PG, Parental Guidance Suggested.</td>
</tr>
<tr>
<td>4</td>
<td>The rating is PG-13, Parental Guidance Suggested, not recommended for those under 13.</td>
</tr>
<tr>
<td>6</td>
<td>The rating is R, Restricted.</td>
</tr>
<tr>
<td>7</td>
<td>The rating is NC-17.</td>
</tr>
</table>
 


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method returns an error unless the domain is DVD_DOMAIN_Stop. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.

This method sets the current user's access level; this access level determines what media files the user can play back. Higher levels can play lower-level content; lower levels can't play higher-level content. For example, adults can watch child-safe content, but children can't watch adult content.

The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> filter provides no restriction on setting the parental level. DVD player applications can enforce restrictions on the parental level setting, such as providing password protection for raising the current parental level. Parental management in the DVD Navigator is disabled by default.

To disable parental management, pass 0xffffffff for <i>ulParentalLevel</i>. If parental management is disabled, then the player will play the first program chain (PGC) in a parental block regardless of parental IDs.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>



<a href="https://msdn.microsoft.com/fc79ad9b-4044-4a33-83b4-f3033283058a">IDvdControl::ParentalCountrySelect</a>
 

 

