---
UID: NF:faxcomex.IFaxOutgoingQueue.Refresh
title: IFaxOutgoingQueue::Refresh (faxcomex.h)
author: windows-sdk-content
description: The IFaxOutgoingQueue::Refresh method refreshes FaxOutgoingQueue object information from the fax server. When the IFaxOutgoingQueue::Refresh method is called, any configuration changes made after the last IFaxOutgoingQueue::Save method call are lost.
old-location: fax\_mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4my0.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxOutgoingQueue interface [Fax Service],Refresh method, IFaxOutgoingQueue.Refresh, IFaxOutgoingQueue::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxOutgoingQueue interface, _mfax_faxoutgoingqueue.refresh, fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_refresh_cpp, fax._mfax_faxoutgoingqueue_refresh, faxcomex/IFaxOutgoingQueue::Refresh
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
 - IFaxOutgoingQueue.Refresh
 - IFaxOutgoingQueue.Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingQueue::Refresh


## -description


The <b>IFaxOutgoingQueue::Refresh</b> method refreshes <a href="https://msdn.microsoft.com/en-us/library/ms687528(v=VS.85).aspx">FaxOutgoingQueue</a> object information from the fax server. When the <b>IFaxOutgoingQueue::Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/en-us/library/ms689100(v=VS.85).aspx">IFaxOutgoingQueue::Save</a> method call are lost.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms687528(v=VS.85).aspx">FaxOutgoingQueue</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687529(v=VS.85).aspx">IFaxOutgoingQueue</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693393(v=VS.85).aspx">Managing Outgoing Jobs</a>
 

 

