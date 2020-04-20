---
UID: NF:control.IDeferredCommand.Confidence
title: IDeferredCommand::Confidence (control.h)
description: The Confidence method retrieves a confidence value that indicates how likely it is for the command to be invoked at the requested time.helpviewer_keywords: ["Confidence","Confidence method [DirectShow]","Confidence method [DirectShow]","IDeferredCommand interface","IDeferredCommand interface [DirectShow]","Confidence method","IDeferredCommand.Confidence","IDeferredCommand::Confidence","IDeferredCommandConfidence","control/IDeferredCommand::Confidence","dshow.ideferredcommand_confidence"]
old-location: dshow\ideferredcommand_confidence.htm
tech.root: DirectShow
ms.assetid: fb3e97a5-b9bc-4a72-9ee7-0a6292fad99d
ms.date: 12/05/2018
ms.keywords: Confidence, Confidence method [DirectShow], Confidence method [DirectShow],IDeferredCommand interface, IDeferredCommand interface [DirectShow],Confidence method, IDeferredCommand.Confidence, IDeferredCommand::Confidence, IDeferredCommandConfidence, control/IDeferredCommand::Confidence, dshow.ideferredcommand_confidence
f1_keywords:
- control/IDeferredCommand.Confidence
dev_langs:
- c++
req.header: control.h
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
- IDeferredCommand.Confidence
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDeferredCommand::Confidence


## -description



The <code>Confidence</code> method retrieves a confidence value that indicates how likely it is for the command to be invoked at the requested time.



This method is not implemented and returns E_NOTIMPL.


## -parameters




### -param pConfidence

Receives the confidence level, on a scale of 0 to 100.


## -returns



Returns E_NOTIMPL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-ideferredcommand">IDeferredCommand Interface</a>
 

 

