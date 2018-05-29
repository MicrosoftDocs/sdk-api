---
UID: NF:strmif.IAMCameraControl.Set
title: IAMCameraControl::Set
author: windows-sdk-content
description: The Set method sets a specified property on the camera.
old-location: dshow\iamcameracontrol_set.htm
old-project: DirectShow
ms.assetid: d896fb5e-a43b-4cb8-a5d1-4ce6e60831be
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IAMCameraControl interface [DirectShow],Set method, IAMCameraControl.Set, IAMCameraControl::Set, IAMCameraControlSet, Set, Set method [DirectShow], Set method [DirectShow],IAMCameraControl interface, dshow.iamcameracontrol_set, strmif/IAMCameraControl::Set
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMCameraControl.Set
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMCameraControl::Set


## -description



The <b>Set</b> method sets a specified property on the camera.




## -parameters




### -param Property [in]

Specifies the property to set, as a value from the <a href="https://msdn.microsoft.com/eebf2246-960f-48ea-86b7-7542e69f2e3e">CameraControlProperty</a> enumeration.
          


### -param lValue [in]

Specifies the new value of the property.
          


### -param Flags [in]

Specifies the desired control setting, as a member of the <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a> enumeration.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the <i>Flags</i> parameter is <b>CameraControl_Flags_Auto</b>, the method ignores the <i>lValue</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/f789db78-292e-4092-a5dc-1906845fb1dd">Configure the Video Quality</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/22bc35f1-76d4-4881-91d1-72f05c24561d">IAMCameraControl Interface</a>



<a href="https://msdn.microsoft.com/5a21f207-5fbb-44b2-82d2-89be29dbdf2c">IAMCameraControl::Get</a>
 

 

