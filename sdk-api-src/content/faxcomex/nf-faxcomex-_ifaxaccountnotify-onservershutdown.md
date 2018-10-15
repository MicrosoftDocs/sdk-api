---
UID: NF:faxcomex._IFaxAccountNotify.OnServerShutDown
title: "_IFaxAccountNotify::OnServerShutDown"
author: windows-sdk-content
description: Called by the fax service when it shuts down.
old-location: fax\_mfax_ifaxaccountnotify_onservershutdown.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountnotify\onservershutdown.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IFaxAccountNotify.OnServerShutDown, OnServerShutDown, OnServerShutDown method [Fax Service], OnServerShutDown method [Fax Service],_IFaxAccountNotify interface, _IFaxAccountNotify interface [Fax Service],OnServerShutDown method, _IFaxAccountNotify.OnServerShutDown, _IFaxAccountNotify::OnServerShutDown, _mfax_ifaxaccountnotify_onservershutdown, fax._mfax_ifaxaccountnotify_onservershutdown, faxcomex/_IFaxAccountNotify::OnServerShutDown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _IFaxAccountNotify::OnServerShutDown


## -description


Called by the fax service when it shuts down. 


## -parameters




### -param pFaxServer

TBD




#### - pFaxAccount

Type: <b><a href="https://msdn.microsoft.com/438a35bd-d08b-4b29-95e5-81ff5c23e92b">IFaxAccount</a>*</b>

A <a href="https://msdn.microsoft.com/438a35bd-d08b-4b29-95e5-81ff5c23e92b">IFaxAccount</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To implement this functionality in Visual Basic, select and implement the appropriate event procedure.




## -see-also




<a href="https://msdn.microsoft.com/ebd959d0-516c-46a0-95cc-78aa49d50cc1">IFaxServerNotify2</a>



<a href="https://msdn.microsoft.com/10867869-66bb-4e17-a9b3-7e943fe5f510">_IFaxAccountNotify</a>
 

 

