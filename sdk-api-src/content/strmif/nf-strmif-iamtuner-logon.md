---
UID: NF:strmif.IAMTuner.Logon
title: IAMTuner::Logon (strmif.h)
description: The Logon method logs a user onto the system.
old-location: dshow\iamtuner_logon.htm
tech.root: DirectShow
ms.assetid: b4a5a927-254c-44cd-b17d-e1f47b3f62a7
ms.date: 12/05/2018
ms.keywords: IAMTuner interface [DirectShow],Logon method, IAMTuner.Logon, IAMTuner::Logon, IAMTunerLogon, Logon, Logon method [DirectShow], Logon method [DirectShow],IAMTuner interface, dshow.iamtuner_logon, strmif/IAMTuner::Logon
ms.topic: method
f1_keywords:
- strmif/IAMTuner.Logon
dev_langs:
- c++
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
- IAMTuner.Logon
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMTuner::Logon


## -description



The <code>Logon</code> method logs a user onto the system.




## -parameters




### -param hCurrentUser [in]

Handle to an application-defined data structure that identifies the current user.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The <code>Logon</code> and <b>Logout</b> methods enable you to implement selective user access.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>
 

 

