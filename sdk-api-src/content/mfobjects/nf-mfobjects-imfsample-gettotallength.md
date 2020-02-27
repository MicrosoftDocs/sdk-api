---
UID: NF:mfobjects.IMFSample.GetTotalLength
title: IMFSample::GetTotalLength (mfobjects.h)
description: Retrieves the total length of the valid data in all of the buffers in the sample. The length is calculated as the sum of the values retrieved by the IMFMediaBuffer::GetCurrentLength method.
old-location: mf\imfsample_gettotallength.htm
tech.root: medfound
ms.assetid: e0dfc1d2-ec78-4d1c-992d-3a876b600ca6
ms.date: 12/05/2018
ms.keywords: GetTotalLength, GetTotalLength method [Media Foundation], GetTotalLength method [Media Foundation],IMFSample interface, IMFSample interface [Media Foundation],GetTotalLength method, IMFSample.GetTotalLength, IMFSample::GetTotalLength, e0dfc1d2-ec78-4d1c-992d-3a876b600ca6, mf.imfsample_gettotallength, mfobjects/IMFSample::GetTotalLength
f1_keywords:
- mfobjects/IMFSample.GetTotalLength
dev_langs:
- c++
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFSample.GetTotalLength
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSample::GetTotalLength


## -description



Retrieves the total length of the valid data in all of the buffers in the sample. The length is calculated as the sum of the values retrieved by the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength">IMFMediaBuffer::GetCurrentLength</a> method.




## -parameters




### -param pcbTotalLength [out]

Receives the total length of the valid data, in bytes.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-samples">Media Samples</a>
 

 

