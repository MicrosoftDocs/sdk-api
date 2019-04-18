---
UID: NF:faxcomex._IFaxServerNotify2.OnIncomingArchiveConfigChange
title: "_IFaxServerNotify2::OnIncomingArchiveConfigChange" (faxcomex.h)
author: windows-sdk-content
description: The fax service calls the IFaxServerNotify2::OnIncomingArchiveConfigChange method when there is a configuration change related to the incoming fax archive.
old-location: fax\_mfax_ifaxservernotify2_onincomingarchiveconfigchange.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_onincomingarchiveconfigchange.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxServerNotify2 interface [Fax Service],OnIncomingArchiveConfigChange method, IFaxServerNotify2.OnIncomingArchiveConfigChange, IFaxServerNotify2::OnIncomingArchiveConfigChange, OnIncomingArchiveConfigChange, OnIncomingArchiveConfigChange method [Fax Service], OnIncomingArchiveConfigChange method [Fax Service],IFaxServerNotify2 interface, _IFaxServerNotify2.OnIncomingArchiveConfigChange, _IFaxServerNotify2::OnIncomingArchiveConfigChange, _mfax_ifaxservernotify2_onincomingarchiveconfigchange, fax._mfax_ifaxservernotify2_onincomingarchiveconfigchange, faxcomex/IFaxServerNotify2::OnIncomingArchiveConfigChange
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
 - IFaxServerNotify2.OnIncomingArchiveConfigChange
 - IFaxServerNotify2.OnIncomingArchiveConfigChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# _IFaxServerNotify2::OnIncomingArchiveConfigChange


## -description


The fax service calls the <b>IFaxServerNotify2::OnIncomingArchiveConfigChange</b> method when there is a configuration change related to the incoming fax archive.


## -parameters




### -param pFaxServer

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa358976(v=VS.85).aspx">IFaxServer2</a>*</b>

A <a href="https://msdn.microsoft.com/en-us/library/Aa358976(v=VS.85).aspx">IFaxServer2</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To implement this functionality in Visual Basic, select and implement the appropriate event procedure. For an example, see <a href="https://msdn.microsoft.com/en-us/library/ms693013(v=VS.85).aspx">Registering for Fax Events</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa358971(v=VS.85).aspx">IFaxServerNotify2</a>
 

 

