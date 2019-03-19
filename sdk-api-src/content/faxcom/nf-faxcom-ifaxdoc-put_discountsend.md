---
UID: NF:faxcom.IFaxDoc.put_DiscountSend
title: IFaxDoc::put_DiscountSend (faxcom.h)
author: windows-sdk-content
description: Sets or retrieves the DiscountSend property for a FaxDoc object. The DiscountSend property is a Boolean value that indicates whether the fax server transmits faxes during the discount period.
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_discountsend_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_2usk.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DiscountSend property [Fax Service], DiscountSend property [Fax Service],IFaxDoc interface, IFaxDoc interface [Fax Service],DiscountSend property, IFaxDoc.DiscountSend, IFaxDoc.put_DiscountSend, IFaxDoc::DiscountSend, IFaxDoc::get_DiscountSend, IFaxDoc::put_DiscountSend, _mfax_ifaxdoc_get_discountsend, fax._mfax_ifaxdoc_get_discountsend, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_discountsend_cpp, faxcom/IFaxDoc::DiscountSend, faxcom/IFaxDoc::get_DiscountSend, faxcom/IFaxDoc::put_DiscountSend, put_DiscountSend
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
 - IFaxDoc.DiscountSend
 - IFaxDoc.get_DiscountSend
 - IFaxDoc.put_DiscountSend
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDoc::put_DiscountSend


## -description


Sets or retrieves the <b>DiscountSend</b> property for a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>DiscountSend</b> property is a Boolean value that indicates whether the fax server transmits faxes during the discount period.

This property is read/write.


## -parameters


## -remarks



To determine the period during which the discount rate applies, you can call the following <a href="https://msdn.microsoft.com/en-us/library/ms692375(v=VS.85).aspx">IFaxServer</a> methods: <a href="https://msdn.microsoft.com/en-us/library/ms691308(v=VS.85).aspx">DiscountRateStartMinute</a>, <a href="https://msdn.microsoft.com/en-us/library/ms690899(v=VS.85).aspx">DiscountRateEndMinute</a>, <a href="https://msdn.microsoft.com/en-us/library/ms690858(v=VS.85).aspx">DiscountRateStartHour</a>, and <a href="https://msdn.microsoft.com/en-us/library/ms691317(v=VS.85).aspx">DiscountRateEndHour</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691317(v=VS.85).aspx">DiscountRateEndHour</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690899(v=VS.85).aspx">DiscountRateEndMinute</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690858(v=VS.85).aspx">DiscountRateStartHour</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691308(v=VS.85).aspx">DiscountRateStartMinute</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692281(v=VS.85).aspx">IFaxDoc</a>
 

 

