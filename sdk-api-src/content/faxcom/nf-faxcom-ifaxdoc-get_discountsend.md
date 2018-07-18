---
UID: NF:faxcom.IFaxDoc.get_DiscountSend
title: IFaxDoc::get_DiscountSend
author: windows-sdk-content
description: Sets or retrieves the DiscountSend property for a FaxDoc object. The DiscountSend property is a Boolean value that indicates whether the fax server transmits faxes during the discount period.
old-location: fax\_mfax_ifaxdoc_get_discountsend_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_2usk.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: DiscountSend property [Fax Service], DiscountSend property [Fax Service],FaxDoc object, FaxDoc object [Fax Service],DiscountSend property, FaxDoc.DiscountSend, IFaxDoc.get_DiscountSend, IFaxDoc::get_DiscountSend, _mfax_ifaxdoc_get_discountsend, fax._mfax_ifaxdoc_get_discountsend, fax._mfax_ifaxdoc_get_discountsend_vb, get_DiscountSend
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ShellWindowTypeConstants
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - FaxDoc.DiscountSend
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDoc::get_DiscountSend


## -description


Sets or retrieves the <b>DiscountSend</b> property for a <a href="https://msdn.microsoft.com/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>DiscountSend</b> property is a Boolean value that indicates whether the fax server transmits faxes during the discount period.

This property is read/write.


## -parameters


## -remarks



To determine the period during which the discount rate applies, you can call the following <a href="https://msdn.microsoft.com/library/ms692375(v=VS.85).aspx">IFaxServer</a> methods: <a href="https://msdn.microsoft.com/library/ms691308(v=VS.85).aspx">DiscountRateStartMinute</a>, <a href="https://msdn.microsoft.com/library/ms690899(v=VS.85).aspx">DiscountRateEndMinute</a>, <a href="https://msdn.microsoft.com/library/ms690858(v=VS.85).aspx">DiscountRateStartHour</a>, and <a href="https://msdn.microsoft.com/library/ms691317(v=VS.85).aspx">DiscountRateEndHour</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/ms691317(v=VS.85).aspx">DiscountRateEndHour</a>



<a href="https://msdn.microsoft.com/library/ms690899(v=VS.85).aspx">DiscountRateEndMinute</a>



<a href="https://msdn.microsoft.com/library/ms690858(v=VS.85).aspx">DiscountRateStartHour</a>



<a href="https://msdn.microsoft.com/library/ms691308(v=VS.85).aspx">DiscountRateStartMinute</a>



<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690707(v=VS.85).aspx">FaxDoc</a>



<a href="https://msdn.microsoft.com/library/ms692281(v=VS.85).aspx">IFaxDoc</a>
 

 

