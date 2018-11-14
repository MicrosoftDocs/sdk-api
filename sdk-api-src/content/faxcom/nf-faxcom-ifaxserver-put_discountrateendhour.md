---
UID: NF:faxcom.IFaxServer.put_DiscountRateEndHour
title: IFaxServer::put_DiscountRateEndHour
author: windows-sdk-content
description: Sets or retrieves the DiscountRateEndHour property for a FaxServer object. The DiscountRateEndHour property is a number that represents the hour the discount period ends. The discount period applies only to outgoing fax transmissions.
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_discountrateendhour_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_2g4y.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: DiscountRateEndHour property [Fax Service], DiscountRateEndHour property [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],DiscountRateEndHour property, IFaxServer.DiscountRateEndHour, IFaxServer.get_DiscountRateEndHour, IFaxServer.put_DiscountRateEndHour, IFaxServer::DiscountRateEndHour, IFaxServer::get_DiscountRateEndHour, IFaxServer::put_DiscountRateEndHour, _mfax_ifaxserver_get_discountrateendhour, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_discountrateendhour_cpp, fax._mfax_ifaxserver_get_discountrateendhour, faxcom/IFaxServer::DiscountRateEndHour, faxcom/IFaxServer::get_DiscountRateEndHour, faxcom/IFaxServer::put_DiscountRateEndHour, put_DiscountRateEndHour
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
 - IFaxServer.DiscountRateEndHour
 - IFaxServer.get_DiscountRateEndHour
 - IFaxServer.put_DiscountRateEndHour
 - IFaxServer.get_DiscountRateEndHour
 - IFaxServer.put_DiscountRateEndHour
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcom.h
: 
- IFaxServer.put_DiscountRateEndHour
: 
---

# IFaxServer::put_DiscountRateEndHour


## -description


Sets or retrieves the <b>DiscountRateEndHour</b> property for a <a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a> object. The <b>DiscountRateEndHour</b> property is a number that represents the hour the discount period ends. The discount period applies only to outgoing fax transmissions.

This property is read/write.


## -parameters


## -remarks



To save on transmission costs, a user can queue a fax job and request that the fax server send the transmission during the discount rate period. For more information, see <a href="https://msdn.microsoft.com/d908fa0c-8fd4-469c-9c4c-b96463b2212e">IFaxDoc::DiscountSend Property</a>.
			

The <a href="https://msdn.microsoft.com/b144d4db-bd0e-4198-8653-6b22013c3d2e">DiscountRateStartHour</a>, <a href="https://msdn.microsoft.com/98355801-ad54-4b1e-a2f2-dcd22ede26e2">DiscountRateStartMinute</a>, <b>DiscountRateEndHour</b>, and <a href="https://msdn.microsoft.com/a8e1bf04-7fc4-48b3-8682-b06c550122a7">DiscountRateEndMinute</a> properties represent local time.
			

If the time the discount rate period ends is less than the time the discount rate period begins, the discount rate period extends into the next day. For example, if the discount rate period begins at 9:00 P.M. and ends at 7:00 A.M., the discount rate period begins in the evening and continues until the morning of the following day.
			




## -see-also




<a href="https://msdn.microsoft.com/d908fa0c-8fd4-469c-9c4c-b96463b2212e">DiscountSend</a>



<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/e3169385-6a7f-4b2d-ad70-6d4d323becb8">FaxServer</a>



<a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a>



<a href="https://msdn.microsoft.com/a8e1bf04-7fc4-48b3-8682-b06c550122a7">IFaxServer::get_DiscountRateEndMinute</a>



<a href="https://msdn.microsoft.com/b144d4db-bd0e-4198-8653-6b22013c3d2e">IFaxServer::get_DiscountRateStartHour</a>



<a href="https://msdn.microsoft.com/98355801-ad54-4b1e-a2f2-dcd22ede26e2">IFaxServer::get_DiscountRateStartMinute</a>
 

 

