---
UID: NF:faxcomex.IFaxOutgoingQueue.Refresh
title: IFaxOutgoingQueue::Refresh
author: windows-sdk-content
description: The IFaxOutgoingQueue::Refresh method refreshes FaxOutgoingQueue object information from the fax server. When the IFaxOutgoingQueue::Refresh method is called, any configuration changes made after the last IFaxOutgoingQueue::Save method call are lost.
old-location: fax\_mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4my0.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxOutgoingQueue interface [Fax Service],Refresh method, IFaxOutgoingQueue.Refresh, IFaxOutgoingQueue::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxOutgoingQueue interface, _mfax_faxoutgoingqueue.refresh, fax._mfax_faxoutgoingqueue_cpp_mfax_faxoutgoingqueue_refresh_cpp, fax._mfax_faxoutgoingqueue_refresh, faxcomex/IFaxOutgoingQueue::Refresh
ms.prod: windows-hardware
ms.technology: windows-devices
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
- apiref
: 
- COM
: 
- faxcomex.h
: 
- IFaxOutgoingQueue.Refresh
: 
---

# IFaxOutgoingQueue::Refresh


## -description


The <b>IFaxOutgoingQueue::Refresh</b> method refreshes <a href="https://msdn.microsoft.com/bad77c9e-2ae5-41a6-ace3-b4b92eb66cc2">FaxOutgoingQueue</a> object information from the fax server. When the <b>IFaxOutgoingQueue::Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/cbb71582-cff9-4bba-aea8-9c88be61ea47">IFaxOutgoingQueue::Save</a> method call are lost.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/bad77c9e-2ae5-41a6-ace3-b4b92eb66cc2">FaxOutgoingQueue</a>



<a href="https://msdn.microsoft.com/2a6fede7-3fb8-495a-a8b1-81b53a701a16">IFaxOutgoingQueue</a>



<a href="https://msdn.microsoft.com/5fab26c3-99f6-4740-9899-3dccbd26a3ba">Managing Outgoing Jobs</a>
 

 

