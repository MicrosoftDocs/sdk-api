---
UID: NF:strmif.IDvdInfo.GetTitleParentalLevels
title: IDvdInfo::GetTitleParentalLevels
author: windows-sdk-content
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the parental levels that are defined for a particular title.
old-location: dshow\idvdinfo_gettitleparentallevels.htm
old-project: DirectShow
ms.assetid: 1a843346-9e24-4321-971f-07e4eed3fc72
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetTitleParentalLevels, GetTitleParentalLevels method [DirectShow], GetTitleParentalLevels method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetTitleParentalLevels method, IDvdInfo.GetTitleParentalLevels, IDvdInfo::GetTitleParentalLevels, IDvdInfoGetTitleParentalLevels, dshow.idvdinfo_gettitleparentallevels, strmif/IDvdInfo::GetTitleParentalLevels
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
 - IDvdInfo.GetTitleParentalLevels
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdInfo::GetTitleParentalLevels


## -description



<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/da30d3dc-feec-4f54-b2db-a771ce404286">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the parental levels that are defined for a particular title.




## -parameters




### -param ulTitle [in]

Title for which parental levels are requested.


### -param pulParentalLevels






#### - pParentalLevels [out]

Pointer to a logical OR combination of the parental levels defined for the title. A higher setting will block out more content than a lower setting. Valid parental levels are the following:

<ul>
<li>DVD_PARENTAL_LEVEL_1</li>
<li>DVD_PARENTAL_LEVEL_2</li>
<li>DVD_PARENTAL_LEVEL_3</li>
<li>DVD_PARENTAL_LEVEL_4</li>
<li>DVD_PARENTAL_LEVEL_5</li>
<li>DVD_PARENTAL_LEVEL_6</li>
<li>DVD_PARENTAL_LEVEL_7</li>
<li>DVD_PARENTAL_LEVEL_8</li>
</ul>

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
 

 

