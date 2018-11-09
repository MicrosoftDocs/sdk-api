---
UID: NF:faxcom.IFaxServer.get_DirtyDays
title: IFaxServer::get_DirtyDays
author: windows-sdk-content
description: Sets or retrieves the DirtyDays property for a FaxServer object. The DirtyDays property is the number of days the fax server retains an unsent job in the fax job queue.
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_dirtydays_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_4nqr.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: DirtyDays property [Fax Service], DirtyDays property [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],DirtyDays property, IFaxServer.DirtyDays, IFaxServer.get_DirtyDays, IFaxServer.put_DirtyDays, IFaxServer::DirtyDays, IFaxServer::get_DirtyDays, IFaxServer::put_DirtyDays, _mfax_ifaxserver_get_dirtydays, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_dirtydays_cpp, fax._mfax_ifaxserver_get_dirtydays, faxcom/IFaxServer::DirtyDays, faxcom/IFaxServer::get_DirtyDays, faxcom/IFaxServer::put_DirtyDays, get_DirtyDays
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcom.h
req.include-header: 
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
req.lib: 
req.dll: Faxcom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxServer.DirtyDays
 - IFaxServer.get_DirtyDays
 - IFaxServer.put_DirtyDays
 - IFaxServer.get_DirtyDays
 - IFaxServer.put_DirtyDays
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxServer::get_DirtyDays


## -description


Sets or retrieves the <b>DirtyDays</b> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>DirtyDays</b> property is the number of days the fax server retains an unsent job in the fax job queue.

This property is read/write.


## -parameters


## -remarks



To minimize the amount of space unsent jobs use, the fax server removes unsent jobs after the number of days specified by the <b>DirtyDays</b> property have elapsed. 

A transmission might not be sent for various reasons. Examples are if an invalid fax number is specified, or when the sending device receives a busy signal multiple times.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a>



<a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a>
 

 

