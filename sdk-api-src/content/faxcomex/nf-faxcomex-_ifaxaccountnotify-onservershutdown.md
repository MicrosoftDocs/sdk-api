---
UID: NF:faxcomex._IFaxAccountNotify.OnServerShutDown
title: _IFaxAccountNotify::OnServerShutDown (faxcomex.h)
description: Called by the fax service when it shuts down.helpviewer_keywords: ["IFaxAccountNotify.OnServerShutDown","OnServerShutDown","OnServerShutDown method [Fax Service]","OnServerShutDown method [Fax Service]","_IFaxAccountNotify interface","_IFaxAccountNotify interface [Fax Service]","OnServerShutDown method","_IFaxAccountNotify.OnServerShutDown","_IFaxAccountNotify::OnServerShutDown","_mfax_ifaxaccountnotify_onservershutdown","fax._mfax_ifaxaccountnotify_onservershutdown","faxcomex/_IFaxAccountNotify::OnServerShutDown"]
old-location: fax\_mfax_ifaxaccountnotify_onservershutdown.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountnotify\onservershutdown.htm
ms.date: 12/05/2018
ms.keywords: IFaxAccountNotify.OnServerShutDown, OnServerShutDown, OnServerShutDown method [Fax Service], OnServerShutDown method [Fax Service],_IFaxAccountNotify interface, _IFaxAccountNotify interface [Fax Service],OnServerShutDown method, _IFaxAccountNotify.OnServerShutDown, _IFaxAccountNotify::OnServerShutDown, _mfax_ifaxaccountnotify_onservershutdown, fax._mfax_ifaxaccountnotify_onservershutdown, faxcomex/_IFaxAccountNotify::OnServerShutDown
f1_keywords:
- faxcomex/_IFaxAccountNotify.OnServerShutDown
dev_langs:
- c++
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Fxscomex.dll
api_name:
- _IFaxAccountNotify.OnServerShutDown
- IFaxAccountNotify.OnServerShutDown
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# _IFaxAccountNotify::OnServerShutDown


## -description


Called by the fax service when it shuts down. 


## -parameters




### -param pFaxServer

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a>*</b>

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxaccount">IFaxAccount</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To implement this functionality in Visual Basic, select and implement the appropriate event procedure.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nn-faxcomex-_ifaxservernotify2">IFaxServerNotify2</a>



<a href="https://docs.microsoft.com/windows/win32/api/faxcomex/nn-faxcomex-_ifaxaccountnotify">_IFaxAccountNotify</a>
 

 

