---
UID: NF:strmif.IAMTuner.Logon
title: IAMTuner::Logon (strmif.h)
description: The Logon method logs a user onto the system.
helpviewer_keywords: ["IAMTuner interface [DirectShow]","Logon method","IAMTuner.Logon","IAMTuner::Logon","IAMTunerLogon","Logon","Logon method [DirectShow]","Logon method [DirectShow]","IAMTuner interface","dshow.iamtuner_logon","strmif/IAMTuner::Logon"]
old-location: dshow\iamtuner_logon.htm
tech.root: dshow
ms.assetid: b4a5a927-254c-44cd-b17d-e1f47b3f62a7
ms.date: 12/05/2018
ms.keywords: IAMTuner interface [DirectShow],Logon method, IAMTuner.Logon, IAMTuner::Logon, IAMTunerLogon, Logon, Logon method [DirectShow], Logon method [DirectShow],IAMTuner interface, dshow.iamtuner_logon, strmif/IAMTuner::Logon
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMTuner::Logon
 - strmif/IAMTuner::Logon
dev_langs:
 - c++
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

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>