---
UID: NF:faxcom.IFaxServer.put_DiscountRateEndMinute
title: IFaxServer::put_DiscountRateEndMinute
author: windows-sdk-content
description: Sets or retrieves the DiscountRateEndMinute property for a FaxServer object. The DiscountRateEndMinute property is a number that represents the minute the discount period ends. The discount period applies only to outgoing fax transmissions.
old-location: fax\_mfax_ifaxserver_client_mfax_ifaxserver_get_discountrateendminute_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1o4l.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DiscountRateEndMinute property [Fax Service], DiscountRateEndMinute property [Fax Service],IFaxServer interface, IFaxServer interface [Fax Service],DiscountRateEndMinute property, IFaxServer.DiscountRateEndMinute, IFaxServer.get_DiscountRateEndMinute, IFaxServer.put_DiscountRateEndMinute, IFaxServer::DiscountRateEndMinute, IFaxServer::get_DiscountRateEndMinute, IFaxServer::put_DiscountRateEndMinute, _mfax_ifaxserver_get_discountrateendminute, fax._mfax_ifaxserver_client_mfax_ifaxserver_get_discountrateendminute_cpp, fax._mfax_ifaxserver_get_discountrateendminute, faxcom/IFaxServer::DiscountRateEndMinute, faxcom/IFaxServer::get_DiscountRateEndMinute, faxcom/IFaxServer::put_DiscountRateEndMinute, put_DiscountRateEndMinute
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
 - IFaxServer.DiscountRateEndMinute
 - IFaxServer.get_DiscountRateEndMinute
 - IFaxServer.put_DiscountRateEndMinute
 - IFaxServer.get_DiscountRateEndMinute
 - IFaxServer.put_DiscountRateEndMinute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxServer::put_DiscountRateEndMinute


## -description


Sets or retrieves the <b>DiscountRateEndMinute</b> property for a <a href="https://msdn.microsoft.com/en-us/library/ms692367(v=VS.85).aspx">FaxServer</a> object. The <b>DiscountRateEndMinute</b> property is a number that represents the minute the discount period ends. The discount period applies only to outgoing fax transmissions.

This property is read/write.


## -parameters


## -remarks



To save on transmission costs, a user can queue a fax job and request that the fax server send the transmission during the discount rate period. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms691359(v=VS.85).aspx">IFaxDoc::DiscountSend Property</a>.
			

The <a href="https://msdn.microsoft.com/en-us/library/ms690858(v=VS.85).aspx">DiscountRateStartHour</a>, <a href="https://msdn.microsoft.com/en-us/library/ms691308(v=VS.85).aspx">DiscountRateStartMinute</a>, <a href="https://msdn.microsoft.com/en-us/library/ms691317(v=VS.85).aspx">DiscountRateEndHour</a>, and <b>DiscountRateEndMinute</b> properties represent local time.
			

If the time the discount rate period ends is less than the time the discount rate period begins, the discount rate period extends into the next day. For example, if the discount rate period begins at 9:00 P.M. and ends at 7:00 A.M., the discount rate period begins in the evening and continues until the morning of the following day.
			




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691359(v=VS.85).aspx">DiscountSend</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692367(v=VS.85).aspx">FaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692375(v=VS.85).aspx">IFaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691317(v=VS.85).aspx">IFaxServer::get_DiscountRateEndHour</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690858(v=VS.85).aspx">IFaxServer::get_DiscountRateStartHour</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691308(v=VS.85).aspx">IFaxServer::get_DiscountRateStartMinute</a>
 

 

