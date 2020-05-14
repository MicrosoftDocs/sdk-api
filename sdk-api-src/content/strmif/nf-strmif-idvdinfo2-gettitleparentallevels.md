---
UID: NF:strmif.IDvdInfo2.GetTitleParentalLevels
title: IDvdInfo2::GetTitleParentalLevels (strmif.h)
description: The GetTitleParentalLevels method retrieves the parental levels that are defined for a particular title.helpviewer_keywords: ["GetTitleParentalLevels","GetTitleParentalLevels method [DirectShow]","GetTitleParentalLevels method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetTitleParentalLevels method","IDvdInfo2.GetTitleParentalLevels","IDvdInfo2::GetTitleParentalLevels","IDvdInfo2GetTitleParentalLevels","dshow.idvdinfo2_gettitleparentallevels","strmif/IDvdInfo2::GetTitleParentalLevels"]
old-location: dshow\idvdinfo2_gettitleparentallevels.htm
tech.root: DirectShow
ms.assetid: 00c9d1e5-1b1f-41b3-b06c-0b78e2d2db0b
ms.date: 12/05/2018
ms.keywords: GetTitleParentalLevels, GetTitleParentalLevels method [DirectShow], GetTitleParentalLevels method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetTitleParentalLevels method, IDvdInfo2.GetTitleParentalLevels, IDvdInfo2::GetTitleParentalLevels, IDvdInfo2GetTitleParentalLevels, dshow.idvdinfo2_gettitleparentallevels, strmif/IDvdInfo2::GetTitleParentalLevels
f1_keywords:
- strmif/IDvdInfo2.GetTitleParentalLevels
dev_langs:
- c++
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IDvdInfo2.GetTitleParentalLevels
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdInfo2::GetTitleParentalLevels


## -description



The <code>GetTitleParentalLevels</code> method retrieves the parental levels that are defined for a particular title.




## -parameters




### -param ulTitle [in]

Title for which parental levels are requested. Specify 0xfffffff to return the parental levels for the current title.


### -param pulParentalLevels [out]

Pointer to a variable of type ULONG that receives a bitwise OR combination of [DVD_PARENTAL_LEVEL](https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_parental_level) values defined for the title.


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
The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> is not initialized.

</td>
</tr>
</table>
 




## -remarks



A title can contain different parental levels for different sections.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/enforcing-parental-management-levels">Enforcing Parental Management Levels</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>
 

 

