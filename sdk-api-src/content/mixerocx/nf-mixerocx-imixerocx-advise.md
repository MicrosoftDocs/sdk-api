---
UID: NF:mixerocx.IMixerOCX.Advise
title: IMixerOCX::Advise
author: windows-sdk-content
description: The Advise method provides the Overlay Mixer with a pointer to the client's IMixerOCXNotify interface for callback notifications.
old-location: dshow\imixerocx_advise.htm
old-project: DirectShow
ms.assetid: 6708fc46-19cb-4843-9c9d-99ff67ee6d08
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: Advise, Advise method [DirectShow], Advise method [DirectShow],IMixerOCX interface, IMixerOCX interface [DirectShow],Advise method, IMixerOCX.Advise, IMixerOCX::Advise, IMixerOCXAdvise, dshow.imixerocx_advise, mixerocx/IMixerOCX::Advise
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mixerocx.h
req.include-header: 
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
req.typenames: WIN32_FIND_DATAW, *PWIN32_FIND_DATAW, *LPWIN32_FIND_DATAW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMixerOCX.Advise
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMixerOCX::Advise


## -description



The <code>Advise</code> method provides the Overlay Mixer with a pointer to the client's <b>IMixerOCXNotify</b> interface for callback notifications.




## -parameters




### -param pmdns [in]

Specifies the client's <a href="https://msdn.microsoft.com/b73416c0-2312-4164-8a6d-f8776dc1447f">IMixerOCXNotify</a> interface.


## -returns



If the method succeeds, it returns S_OK.




## -remarks



Call this method if you wish to receive callbacks from the Overlay Mixer.




## -see-also




<a href="https://msdn.microsoft.com/b80d720d-921d-4d24-a168-49944cfcc411">IMixerOCX Interface</a>



<a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a>
 

 

