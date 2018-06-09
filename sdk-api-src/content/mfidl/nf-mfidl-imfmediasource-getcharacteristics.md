---
UID: NF:mfidl.IMFMediaSource.GetCharacteristics
title: IMFMediaSource::GetCharacteristics
author: windows-sdk-content
description: Retrieves the characteristics of the media source.
old-location: mf\imfmediasource_getcharacteristics.htm
old-project: medfound
ms.assetid: cb5d54cd-58a3-4903-b22e-8207f90dbbc0
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetCharacteristics, GetCharacteristics method [Media Foundation], GetCharacteristics method [Media Foundation],IMFMediaSource interface, IMFMediaSource interface [Media Foundation],GetCharacteristics method, IMFMediaSource.GetCharacteristics, IMFMediaSource::GetCharacteristics, cb5d54cd-58a3-4903-b22e-8207f90dbbc0, mf.imfmediasource_getcharacteristics, mfidl/IMFMediaSource::GetCharacteristics
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaSource.GetCharacteristics
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaSource::GetCharacteristics


## -description



Retrieves the characteristics of the media source.




## -parameters




### -param pdwCharacteristics [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/115f4a6b-99c2-436e-9483-c44003e61a7d">MFMEDIASOURCE_CHARACTERISTICS</a> enumeration.


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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media source's <a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a> method has been called.

</td>
</tr>
</table>
 




## -remarks



The characteristics of a media source can change at any time. If this happens, the source sends an <a href="https://msdn.microsoft.com/df7bb9a3-5949-4a4a-8835-c5b1d01b5cb3">MESourceCharacteristicsChanged</a> event.




## -see-also




<a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a>
 

 

