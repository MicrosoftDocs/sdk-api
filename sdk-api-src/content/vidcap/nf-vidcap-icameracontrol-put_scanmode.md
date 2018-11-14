---
UID: NF:vidcap.ICameraControl.put_ScanMode
title: ICameraControl::put_ScanMode
author: windows-sdk-content
description: The put_ScanMode method sets the camera's scanning mode (interlaced or progressive).
old-location: dshow\icameracontrol_put_scanmode.htm
tech.root: DirectShow
ms.assetid: 74d5d2bd-4aa4-49f6-a02f-c53af1333a1b
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ICameraControl interface [DirectShow],put_ScanMode method, ICameraControl.put_ScanMode, ICameraControl::put_ScanMode, ICameraControlput_ScanMode, dshow.icameracontrol_put_scanmode, put_ScanMode, put_ScanMode method [DirectShow], put_ScanMode method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_ScanMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
 - ICameraControl.put_ScanMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vidcap.h
: 
- ICameraControl.put_ScanMode
: 
---

# ICameraControl::put_ScanMode


## -description


The <code>put_ScanMode</code> method sets the camera's scanning mode (interlaced or progressive).


## -parameters




### -param Value [in]

Specifies one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Interlaced.</td>
</tr>
<tr>
<td>1</td>
<td>Progressive.</td>
</tr>
</table>
 


### -param Flags [in]

Zero or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

