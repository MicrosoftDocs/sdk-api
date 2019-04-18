---
UID: NF:faxcomex.IFaxIncomingQueue.Refresh
title: IFaxIncomingQueue::Refresh (faxcomex.h)
author: windows-sdk-content
description: The Refresh method refreshes FaxIncomingQueue object information from the fax server. When the Refresh method is called, any configuration changes made after the last Save method call are lost.
old-location: fax\_mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_24vc.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxIncomingQueue interface [Fax Service],Refresh method, IFaxIncomingQueue.Refresh, IFaxIncomingQueue::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxIncomingQueue interface, _mfax_faxincomingqueue.refresh, fax._mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_refresh_cpp, fax._mfax_faxincomingqueue_refresh, faxcomex/IFaxIncomingQueue::Refresh
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IFaxIncomingQueue.Refresh
 - IFaxIncomingQueue.Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxIncomingQueue::Refresh


## -description


The <b>Refresh</b> method refreshes <a href="https://msdn.microsoft.com/en-us/library/ms686164(v=VS.85).aspx">FaxIncomingQueue</a> object information from the fax server. When the <b>Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/en-us/library/ms685088(v=VS.85).aspx">Save</a> method call are lost.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686164(v=VS.85).aspx">FaxIncomingQueue</a>



<a href="https://msdn.microsoft.com/en-us/library/ms686165(v=VS.85).aspx">IFaxIncomingQueue</a>
 

 

