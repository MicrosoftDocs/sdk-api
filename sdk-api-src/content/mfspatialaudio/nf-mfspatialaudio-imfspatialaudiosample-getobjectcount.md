---
UID: NF:mfspatialaudio.IMFSpatialAudioSample.GetObjectCount
title: IMFSpatialAudioSample::GetObjectCount
author: windows-sdk-content
description: Gets the count of spatial audio objects, represented by IMFSpatialAudioObjectBuffer objects, in the sample.
old-location: mf\imfspatialaudiosample_getobjectcount.htm
tech.root: medfound
ms.assetid: D386E482-4C5A-4F8A-801F-EA1AD4C9157C
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetObjectCount, GetObjectCount method [Media Foundation], GetObjectCount method [Media Foundation],IMFSpatialAudioSample interface, IMFSpatialAudioSample interface [Media Foundation],GetObjectCount method, IMFSpatialAudioSample.GetObjectCount, IMFSpatialAudioSample::GetObjectCount, mf.imfspatialaudiosample_getobjectcount, mfspatialaudio/IMFSpatialAudioSample::GetObjectCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfspatialaudio.h
req.include-header: Mfobjects.h
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
req.lib: Mfobjects.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.lib
 - mfobjects.dll
api_name:
 - IMFSpatialAudioSample.GetObjectCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSpatialAudioSample::GetObjectCount


## -description


Gets the count of spatial audio objects, represented by <a href="https://msdn.microsoft.com/61E9BC6A-2120-4874-9053-E1D232DF1CCA">IMFSpatialAudioObjectBuffer</a> objects, in the sample.


## -parameters




### -param pdwObjectCount [out]

A pointer to a 32 bit variable where the total number of audio objects in the sample will be stored.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The supplied pointer is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/EA0277BF-C9C8-42FE-9206-A87FC3C50A9F">IMFSpatialAudioSample</a>
 

 

