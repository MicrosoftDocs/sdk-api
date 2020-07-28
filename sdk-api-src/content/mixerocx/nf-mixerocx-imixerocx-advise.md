---
UID: NF:mixerocx.IMixerOCX.Advise
title: IMixerOCX::Advise (mixerocx.h)
description: The Advise method provides the Overlay Mixer with a pointer to the client's IMixerOCXNotify interface for callback notifications.
helpviewer_keywords: ["Advise","Advise method [DirectShow]","Advise method [DirectShow]","IMixerOCX interface","IMixerOCX interface [DirectShow]","Advise method","IMixerOCX.Advise","IMixerOCX::Advise","IMixerOCXAdvise","dshow.imixerocx_advise","mixerocx/IMixerOCX::Advise"]
old-location: dshow\imixerocx_advise.htm
tech.root: dshow
ms.assetid: 6708fc46-19cb-4843-9c9d-99ff67ee6d08
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [DirectShow], Advise method [DirectShow],IMixerOCX interface, IMixerOCX interface [DirectShow],Advise method, IMixerOCX.Advise, IMixerOCX::Advise, IMixerOCXAdvise, dshow.imixerocx_advise, mixerocx/IMixerOCX::Advise
f1_keywords:
- mixerocx/IMixerOCX.Advise
dev_langs:
- c++
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
- IMixerOCX.Advise
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMixerOCX::Advise


## -description



The <code>Advise</code> method provides the Overlay Mixer with a pointer to the client's <b>IMixerOCXNotify</b> interface for callback notifications.




## -parameters




### -param pmdns [in]

Specifies the client's <a href="https://docs.microsoft.com/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify">IMixerOCXNotify</a> interface.


## -returns



If the method succeeds, it returns S_OK.




## -remarks



Call this method if you wish to receive callbacks from the Overlay Mixer.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mixerocx/nn-mixerocx-imixerocx">IMixerOCX Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a>
 

 

