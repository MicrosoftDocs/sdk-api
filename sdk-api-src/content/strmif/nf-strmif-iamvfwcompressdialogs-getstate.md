---
UID: NF:strmif.IAMVfwCompressDialogs.GetState
title: IAMVfwCompressDialogs::GetState
author: windows-driver-content
description: The GetState method retrieves the current configuration settings for the VCM codec currently being used.
old-location: dshow\iamvfwcompressdialogs_getstate.htm
old-project: DirectShow
ms.assetid: a010fd8a-ad4a-4b52-abfe-a2db8cd15b65
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: GetState, GetState method [DirectShow], GetState method [DirectShow],IAMVfwCompressDialogs interface, IAMVfwCompressDialogs interface [DirectShow],GetState method, IAMVfwCompressDialogs.GetState, IAMVfwCompressDialogs::GetState, IAMVfwCompressDialogsGetState, dshow.iamvfwcompressdialogs_getstate, strmif/IAMVfwCompressDialogs::GetState
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IAMVfwCompressDialogs.GetState
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMVfwCompressDialogs::GetState


## -description



The <code>GetState</code> method retrieves the current configuration settings for the VCM codec currently being used.




## -parameters




### -param pState [out]

State of the VCM codec.


### -param pcbState [in, out]

Pointer to the size of the state.


## -returns



Return value varies depending on the implementation within each driver.




## -remarks



This method calls the  <a href="https://msdn.microsoft.com/e0066cc2-a67d-4cf4-9d22-506cc152ec14">ICGetState</a> macro.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/5cc23d68-e0e6-401a-8d16-63c8c68af241">IAMVfwCompressDialogs Interface</a>
 

 

