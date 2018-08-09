---
UID: NF:mfspatialaudio.IMFSpatialAudioSample.AddSpatialAudioObject
title: IMFSpatialAudioSample::AddSpatialAudioObject
author: windows-sdk-content
description: Adds a new spatial audio object, represented by an IMFSpatialAudioObjectBuffer object, to the sample.
old-location: mf\imfspatialaudiosample_addspatialaudioobject.htm
old-project: medfound
ms.assetid: D967B4FE-8E11-4520-BF9E-725ACC7AA99A
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: AddSpatialAudioObject, AddSpatialAudioObject method [Media Foundation], AddSpatialAudioObject method [Media Foundation],IMFSpatialAudioSample interface, IMFSpatialAudioSample interface [Media Foundation],AddSpatialAudioObject method, IMFSpatialAudioSample.AddSpatialAudioObject, IMFSpatialAudioSample::AddSpatialAudioObject, mf.imfspatialaudiosample_addspatialaudioobject, mfspatialaudio/IMFSpatialAudioSample::AddSpatialAudioObject
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DEVICE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.lib
 - mfobjects.dll
api_name:
 - IMFSpatialAudioSample.AddSpatialAudioObject
product: Windows
targetos: Windows
req.lib: Mfobjects.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSpatialAudioSample::AddSpatialAudioObject


## -description


Adds a new spatial audio object, represented by an <a href="https://msdn.microsoft.com/61E9BC6A-2120-4874-9053-E1D232DF1CCA">IMFSpatialAudioObjectBuffer</a> object, to the     sample.


## -parameters




### -param pAudioObjBuffer [in]

A pointer to the new IMFSpatialAudioObject.


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
 

 

