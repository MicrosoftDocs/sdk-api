---
UID: NF:mfobjects.IMFMuxStreamSampleManager.GetSample
title: IMFMuxStreamSampleManager::GetSample
author: windows-sdk-content
description: Gets the IMFSample associated with the substream with the specified index.
old-location: mf\imfmuxstreamsamplemanager_getsample.htm
tech.root: medfound
ms.assetid: F52147C3-FF6D-4F8F-93BE-2A3237C5A827
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetSample, GetSample method [Media Foundation], GetSample method [Media Foundation],IMFMuxStreamSampleManager interface, IMFMuxStreamSampleManager interface [Media Foundation],GetSample method, IMFMuxStreamSampleManager.GetSample, IMFMuxStreamSampleManager::GetSample, mf.imfmuxstreamsamplemanager_getsample, mfobjects/IMFMuxStreamSampleManager::GetSample
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFMuxStreamSampleManager.GetSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMuxStreamSampleManager::GetSample


## -description


Gets the <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a> associated with the substream with the specified index.


## -parameters




### -param dwMuxStreamIndex [in]

The index of the substream for which a sample is retrieved.


### -param ppSample [out]

The retrieved sample.


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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The specified substream index is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMDATA</b></dt>
</dl>
</td>
<td width="60%">
The stream data for the sample is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/DABA5955-1366-4CEE-ABDF-7CC0F3788A8E">IMFMuxStreamSampleManager</a>
 

 

