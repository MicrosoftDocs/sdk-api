---
UID: NF:strmif.IAMTuner.Logon
title: IAMTuner::Logon
author: windows-driver-content
description: The Logon method logs a user onto the system.
old-location: dshow\iamtuner_logon.htm
old-project: DirectShow
ms.assetid: b4a5a927-254c-44cd-b17d-e1f47b3f62a7
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IAMTuner interface [DirectShow],Logon method, IAMTuner.Logon, IAMTuner::Logon, IAMTunerLogon, Logon, Logon method [DirectShow], Logon method [DirectShow],IAMTuner interface, dshow.iamtuner_logon, strmif/IAMTuner::Logon
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
-	IAMTuner.Logon
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

