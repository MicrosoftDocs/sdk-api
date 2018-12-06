---
UID: NF:amvideo.IDirectDrawVideo.SetDefault
title: IDirectDrawVideo::SetDefault
author: windows-sdk-content
description: The SetDefault method makes the current property settings the global default.
old-location: dshow\idirectdrawvideo_setdefault.htm
tech.root: DirectShow
ms.assetid: 9525ee57-3c53-42db-bc40-eb1d4658d9b6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDirectDrawVideo interface [DirectShow],SetDefault method, IDirectDrawVideo.SetDefault, IDirectDrawVideo::SetDefault, IDirectDrawVideoSetDefault, SetDefault, SetDefault method [DirectShow], SetDefault method [DirectShow],IDirectDrawVideo interface, amvideo/IDirectDrawVideo::SetDefault, dshow.idirectdrawvideo_setdefault
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: amvideo.h
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
 - IDirectDrawVideo.SetDefault
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawVideo::SetDefault


## -description



The <code>SetDefault</code> method makes the current property settings the global default.




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



All properties set through <b>IDirectDrawVideo</b> are specific to that particular instance. Call this method to make properties set on this instance of <b>IDirectDrawVideo</b> the global default of all DirectShow instances of this interface. After it is called, the current property settings will persist between the subsequent starting of other DirectShow filter graphs and between any computer restarts.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/b918bf3b-b91b-40fb-abb8-4115a4f254bb">IDirectDrawVideo Interface</a>
 

 

