---
UID: NF:strmif.IDvdInfo2.IsSubpictureStreamEnabled
title: IDvdInfo2::IsSubpictureStreamEnabled (strmif.h)
description: The IsSubpictureStreamEnabled method determines if the specified subpicture stream is enabled in the current title.helpviewer_keywords: ["IDvdInfo2 interface [DirectShow]","IsSubpictureStreamEnabled method","IDvdInfo2.IsSubpictureStreamEnabled","IDvdInfo2::IsSubpictureStreamEnabled","IDvdInfo2IsSubpictureStreamEnabled","IsSubpictureStreamEnabled","IsSubpictureStreamEnabled method [DirectShow]","IsSubpictureStreamEnabled method [DirectShow]","IDvdInfo2 interface","dshow.idvdinfo2_issubpicturestreamenabled","strmif/IDvdInfo2::IsSubpictureStreamEnabled"]
old-location: dshow\idvdinfo2_issubpicturestreamenabled.htm
tech.root: DirectShow
ms.assetid: 19facb38-8bc4-4605-9b2b-2a123b67aeb6
ms.date: 12/05/2018
ms.keywords: IDvdInfo2 interface [DirectShow],IsSubpictureStreamEnabled method, IDvdInfo2.IsSubpictureStreamEnabled, IDvdInfo2::IsSubpictureStreamEnabled, IDvdInfo2IsSubpictureStreamEnabled, IsSubpictureStreamEnabled, IsSubpictureStreamEnabled method [DirectShow], IsSubpictureStreamEnabled method [DirectShow],IDvdInfo2 interface, dshow.idvdinfo2_issubpicturestreamenabled, strmif/IDvdInfo2::IsSubpictureStreamEnabled
f1_keywords:
- strmif/IDvdInfo2.IsSubpictureStreamEnabled
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
- IDvdInfo2.IsSubpictureStreamEnabled
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdInfo2::IsSubpictureStreamEnabled


## -description



The <code>IsSubpictureStreamEnabled</code> method determines if the specified subpicture stream is enabled in the current title.




## -parameters




### -param ulStreamNum [in]

Subpicture stream number to test.


### -param pbEnabled [out]

Pointer to a variable of type BOOL that receives a value of <b>TRUE</b> if the audio stream is enabled, or <b>FALSE</b> otherwise.


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



A DVD can have up to 32 separate subpicture streams, although typically not all the streams will be enabled for each title. Use <code>IsSubpictureStreamEnabled</code> to determine whether a particular stream is enabled for the current title, and then call <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectsubpicturestream">IDvdControl2::SelectSubpictureStream</a> to select one of the enabled streams.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>
 

 

