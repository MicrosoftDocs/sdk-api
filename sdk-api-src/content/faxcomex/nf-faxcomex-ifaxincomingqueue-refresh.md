---
UID: NF:faxcomex.IFaxIncomingQueue.Refresh
title: IFaxIncomingQueue::Refresh
author: windows-sdk-content
description: The Refresh method refreshes FaxIncomingQueue object information from the fax server. When the Refresh method is called, any configuration changes made after the last Save method call are lost.
old-location: fax\_mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_24vc.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IFaxIncomingQueue interface [Fax Service],Refresh method, IFaxIncomingQueue.Refresh, IFaxIncomingQueue::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxIncomingQueue interface, _mfax_faxincomingqueue.refresh, fax._mfax_faxincomingqueue_cpp_mfax_faxincomingqueue_refresh_cpp, fax._mfax_faxincomingqueue_refresh, faxcomex/IFaxIncomingQueue::Refresh
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
 - IFaxIncomingQueue.Refresh
 - IFaxIncomingQueue.Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingQueue::Refresh


## -description


The <b>Refresh</b> method refreshes <a href="https://msdn.microsoft.com/769e4fc5-5607-4fd6-8f78-59b190c94787">FaxIncomingQueue</a> object information from the fax server. When the <b>Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/cf58022f-6f59-4194-a358-1871f032f3f0">Save</a> method call are lost.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/769e4fc5-5607-4fd6-8f78-59b190c94787">FaxIncomingQueue</a>



<a href="https://msdn.microsoft.com/291f8709-c10f-4041-864f-82431edd7fab">IFaxIncomingQueue</a>
 

 

