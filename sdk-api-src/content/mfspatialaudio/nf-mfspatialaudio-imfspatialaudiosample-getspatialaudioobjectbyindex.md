---
UID: NF:mfspatialaudio.IMFSpatialAudioSample.GetSpatialAudioObjectByIndex
title: IMFSpatialAudioSample::GetSpatialAudioObjectByIndex
author: windows-sdk-content
description: Returns the spatial audio object, represented by an IMFSpatialAudioObjectBuffer object, corresponding to the specified index.
old-location: mf\imfspatialaudiosample_getspatialaudioobjectbyindex.htm
tech.root: medfound
ms.assetid: 2B5A2D44-BA41-49FC-B4FD-9BCD9EE2D549
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetSpatialAudioObjectByIndex, GetSpatialAudioObjectByIndex method [Media Foundation], GetSpatialAudioObjectByIndex method [Media Foundation],IMFSpatialAudioSample interface, IMFSpatialAudioSample interface [Media Foundation],GetSpatialAudioObjectByIndex method, IMFSpatialAudioSample.GetSpatialAudioObjectByIndex, IMFSpatialAudioSample::GetSpatialAudioObjectByIndex, mf.imfspatialaudiosample_getspatialaudioobjectbyindex, mfspatialaudio/IMFSpatialAudioSample::GetSpatialAudioObjectByIndex
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
 - IMFSpatialAudioSample.GetSpatialAudioObjectByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfspatialaudio.h
: 
- IMFSpatialAudioSample.GetSpatialAudioObjectByIndex
: 
---

# IMFSpatialAudioSample::GetSpatialAudioObjectByIndex


## -description


Returns the spatial audio object, represented by an <a href="https://msdn.microsoft.com/61E9BC6A-2120-4874-9053-E1D232DF1CCA">IMFSpatialAudioObjectBuffer</a> object, corresponding to the specified index.


## -parameters




### -param dwIndex

A 32 bit variable with the 0-based index of the requested audio object.


### -param ppAudioObjBuffer

TBD




#### - ppSpatialAudioObjectBuffer

A pointer to an <a href="https://msdn.microsoft.com/61E9BC6A-2120-4874-9053-E1D232DF1CCA">IMFSpatialAudioObjectBuffer</a> object in which the spatial audio object corresponding with the specified index will be stored.


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
 

 

