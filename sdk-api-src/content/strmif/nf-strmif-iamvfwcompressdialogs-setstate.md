---
UID: NF:strmif.IAMVfwCompressDialogs.SetState
title: IAMVfwCompressDialogs::SetState
author: windows-sdk-content
description: The SetState method sets configuration for the VCM codec.
old-location: dshow\iamvfwcompressdialogs_setstate.htm
tech.root: DirectShow
ms.assetid: 9b27bbaa-4e2f-4567-a6fc-62fb3f5f31a8
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IAMVfwCompressDialogs interface [DirectShow],SetState method, IAMVfwCompressDialogs.SetState, IAMVfwCompressDialogs::SetState, IAMVfwCompressDialogsSetState, SetState, SetState method [DirectShow], SetState method [DirectShow],IAMVfwCompressDialogs interface, dshow.iamvfwcompressdialogs_setstate, strmif/IAMVfwCompressDialogs::SetState
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
 - IAMVfwCompressDialogs.SetState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVfwCompressDialogs::SetState


## -description



The <code>SetState</code> method sets configuration for the VCM codec.




## -parameters




### -param pState [in]

State of the VCM codec.


### -param cbState [in]

Size of the state.


## -returns



Return value varies depending on the implementation within each driver.




## -remarks



This method calls the <a href="https://msdn.microsoft.com/96958fbf-8539-49bc-a2ff-160b7ea8d2ab">ICSetState</a> macro, which notifies a video compression driver to set the state of the compressor.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/5cc23d68-e0e6-401a-8d16-63c8c68af241">IAMVfwCompressDialogs Interface</a>
 

 

