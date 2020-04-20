---
UID: NF:strmif.IDvdInfo2.GetNumberOfChapters
title: IDvdInfo2::GetNumberOfChapters (strmif.h)
description: The GetNumberOfChapters method retrieves the number of chapters in a given title.helpviewer_keywords: ["GetNumberOfChapters","GetNumberOfChapters method [DirectShow]","GetNumberOfChapters method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetNumberOfChapters method","IDvdInfo2.GetNumberOfChapters","IDvdInfo2::GetNumberOfChapters","IDvdInfo2GetNumberOfChapters","dshow.idvdinfo2_getnumberofchapters","strmif/IDvdInfo2::GetNumberOfChapters"]
old-location: dshow\idvdinfo2_getnumberofchapters.htm
tech.root: DirectShow
ms.assetid: 5899fa87-56e2-4287-9325-1d9eaedb892b
ms.date: 12/05/2018
ms.keywords: GetNumberOfChapters, GetNumberOfChapters method [DirectShow], GetNumberOfChapters method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetNumberOfChapters method, IDvdInfo2.GetNumberOfChapters, IDvdInfo2::GetNumberOfChapters, IDvdInfo2GetNumberOfChapters, dshow.idvdinfo2_getnumberofchapters, strmif/IDvdInfo2::GetNumberOfChapters
f1_keywords:
- strmif/IDvdInfo2.GetNumberOfChapters
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
- IDvdInfo2.GetNumberOfChapters
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdInfo2::GetNumberOfChapters


## -description



The <code>GetNumberOfChapters</code> method retrieves the number of chapters in a given title.




## -parameters




### -param ulTitle [in]

Specifies the title.


### -param pulNumOfChapters [out]

Receives the number of chapters for the specified title.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is invalid.

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



Call this method to get the number of chapters before calling <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-playchapter">IDvdControl2::PlayChapter</a>, to ensure that you specify a valid chapter number.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>
 

 

