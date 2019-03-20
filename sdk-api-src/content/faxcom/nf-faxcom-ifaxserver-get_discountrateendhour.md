---
UID: NF:faxcom.IFaxServer.get_DiscountRateEndHour
title: IFaxServer::get_DiscountRateEndHour (faxcom.h)
author: windows-sdk-content
description: Sets or retrieves the DiscountRateEndHour property for a FaxServer object. The DiscountRateEndHour property is a number that represents the hour the discount period ends. The discount period applies only to outgoing fax transmissions.
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_discountrateendhour_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_2g4y.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DiscountRateEndHour property [Fax Service], DiscountRateEndHour property [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],DiscountRateEndHour property, IFaxServer.DiscountRateEndHour, IFaxServer.get_DiscountRateEndHour, IFaxServer.put_DiscountRateEndHour, IFaxServer::DiscountRateEndHour, IFaxServer::get_DiscountRateEndHour, IFaxServer::put_DiscountRateEndHour, _mfax_ifaxserver_get_discountrateendhour, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_discountrateendhour_cpp, fax._mfax_ifaxserver_get_discountrateendhour, faxcom/IFaxServer::DiscountRateEndHour, faxcom/IFaxServer::get_DiscountRateEndHour, faxcom/IFaxServer::put_DiscountRateEndHour, get_DiscountRateEndHour
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
---

# IFaxServer::get_DiscountRateEndHour


## -description


Sets or retrieves the <b>DiscountRateEndHour</b> property for a <a href="https://msdn.microsoft.com/en-us/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <b>DiscountRateEndHour</b> property is a number that represents the hour the discount period ends. The discount period applies only to outgoing fax transmissions.

This property is read/write.


## -parameters


## -remarks



To save on transmission costs, a user can queue a fax job and request that the fax server send the transmission during the discount rate period. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms691359(v=VS.85).aspx">IFaxDoc::DiscountSend Property</a>.
			

The <a href="https://msdn.microsoft.com/en-us/library/ms690858(v=VS.85).aspx">DiscountRateStartHour</a>, <a href="https://msdn.microsoft.com/en-us/library/ms691308(v=VS.85).aspx">DiscountRateStartMinute</a>, <b>DiscountRateEndHour</b>, and <a href="https://msdn.microsoft.com/en-us/library/ms690899(v=VS.85).aspx">DiscountRateEndMinute</a> properties represent local time.
			

If the time the discount rate period ends is less than the time the discount rate period begins, the discount rate period extends into the next day. For example, if the discount rate period begins at 9:00 P.M. and ends at 7:00 A.M., the discount rate period begins in the evening and continues until the morning of the following day.
			




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691359(v=VS.85).aspx">DiscountSend</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692367(v=VS.85).aspx">FaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692375(v=VS.85).aspx">IFaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690899(v=VS.85).aspx">IFaxServer::get_DiscountRateEndMinute</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690858(v=VS.85).aspx">IFaxServer::get_DiscountRateStartHour</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691308(v=VS.85).aspx">IFaxServer::get_DiscountRateStartMinute</a>
 

 

