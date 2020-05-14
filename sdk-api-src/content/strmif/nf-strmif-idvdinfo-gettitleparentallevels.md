---
UID: NF:strmif.IDvdInfo.GetTitleParentalLevels
title: IDvdInfo::GetTitleParentalLevels (strmif.h)
description: Note  The IDvdInfo interface is deprecated. Use IDvdInfo2 instead. Retrieves the parental levels that are defined for a particular title.helpviewer_keywords: ["GetTitleParentalLevels","GetTitleParentalLevels method [DirectShow]","GetTitleParentalLevels method [DirectShow]","IDvdInfo interface","IDvdInfo interface [DirectShow]","GetTitleParentalLevels method","IDvdInfo.GetTitleParentalLevels","IDvdInfo::GetTitleParentalLevels","IDvdInfoGetTitleParentalLevels","dshow.idvdinfo_gettitleparentallevels","strmif/IDvdInfo::GetTitleParentalLevels"]
old-location: dshow\idvdinfo_gettitleparentallevels.htm
tech.root: DirectShow
ms.assetid: 1a843346-9e24-4321-971f-07e4eed3fc72
ms.date: 12/05/2018
ms.keywords: GetTitleParentalLevels, GetTitleParentalLevels method [DirectShow], GetTitleParentalLevels method [DirectShow],IDvdInfo interface, IDvdInfo interface [DirectShow],GetTitleParentalLevels method, IDvdInfo.GetTitleParentalLevels, IDvdInfo::GetTitleParentalLevels, IDvdInfoGetTitleParentalLevels, dshow.idvdinfo_gettitleparentallevels, strmif/IDvdInfo::GetTitleParentalLevels
f1_keywords:
- strmif/IDvdInfo.GetTitleParentalLevels
dev_langs:
- c++
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
- IDvdInfo.GetTitleParentalLevels
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdInfo::GetTitleParentalLevels


## -description



<div class="alert"><b>Note</b>  The <b>IDvdInfo</b> interface is deprecated. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> instead.</div>
<div> </div>
Retrieves the parental levels that are defined for a particular title.




## -parameters




### -param ulTitle [in]

Title for which parental levels are requested.


### -param pulParentalLevels [out]

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
Requested action is not supported on this domain (<a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>).

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



This method is valid in any domain. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo">IDvdInfo Interface</a>
 

 

