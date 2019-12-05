---
UID: NF:strmif.IDvdInfo2.GetCurrentVideoAttributes
title: IDvdInfo2::GetCurrentVideoAttributes (strmif.h)
description: The GetCurrentVideoAttributes method retrieves the video attributes of the current title or menu.
old-location: dshow\idvdinfo2_getcurrentvideoattributes.htm
tech.root: DirectShow
ms.assetid: 92bd3af9-7057-4bf7-9026-d4862c271a03
ms.date: 12/05/2018
ms.keywords: GetCurrentVideoAttributes, GetCurrentVideoAttributes method [DirectShow], GetCurrentVideoAttributes method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetCurrentVideoAttributes method, IDvdInfo2.GetCurrentVideoAttributes, IDvdInfo2::GetCurrentVideoAttributes, IDvdInfo2GetCurrentVideoAttributes, dshow.idvdinfo2_getcurrentvideoattributes, strmif/IDvdInfo2::GetCurrentVideoAttributes
ms.topic: method
f1_keywords:
- strmif/IDvdInfo2.GetCurrentVideoAttributes
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
- IDvdInfo2.GetCurrentVideoAttributes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdInfo2::GetCurrentVideoAttributes


## -description



The <code>GetCurrentVideoAttributes</code> method retrieves the video attributes of the current title or menu.




## -parameters




### -param pATR [out]

Pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ns-strmif-dvd_videoattributes">DVD_VideoAttributes</a> structure that receives the attributes.


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
<dt><b>E_POINTER</b></dt>
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



The use of this method is demonstrated in the DVDSample application in <b>CDvdCore::GetVideoAttributes()</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>
 

 

