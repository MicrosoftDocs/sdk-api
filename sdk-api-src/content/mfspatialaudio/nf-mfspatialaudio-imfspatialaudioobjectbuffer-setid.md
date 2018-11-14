---
UID: NF:mfspatialaudio.IMFSpatialAudioObjectBuffer.SetID
title: IMFSpatialAudioObjectBuffer::SetID
author: windows-sdk-content
description: Sets the ID of the spatial audio object represented by the buffer.
old-location: mf\imfspatialaudioobjectbuffer_setid.htm
tech.root: medfound
ms.assetid: 01979492-2CA1-4DAA-8B03-720B521C2D9A
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IMFSpatialAudioObjectBuffer interface [Media Foundation],SetID method, IMFSpatialAudioObjectBuffer.SetID, IMFSpatialAudioObjectBuffer::SetID, SetID, SetID method [Media Foundation], SetID method [Media Foundation],IMFSpatialAudioObjectBuffer interface, mf.imfspatialaudioobjectbuffer_setid, mfspatialaudio/IMFSpatialAudioObjectBuffer::SetID
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
 - IMFSpatialAudioObjectBuffer.SetID
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
- IMFSpatialAudioObjectBuffer.SetID
: 
---

# IMFSpatialAudioObjectBuffer::SetID


## -description


Sets the ID of the spatial audio object represented by the buffer.


## -parameters




### -param u32ID

A 32-bit unsigned unique ID of the audio object.


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



The object ID must be unique for each spatial audio sample.  Subsequent samples can 
    contain spatial audio objects with the same IDs to represent moving dynamic objects or constant
    static objects.




## -see-also




<a href="https://msdn.microsoft.com/61E9BC6A-2120-4874-9053-E1D232DF1CCA">IMFSpatialAudioObjectBuffer</a>
 

 

