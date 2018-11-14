---
UID: NF:faxcom.IFaxDoc.get_DiscountSend
title: IFaxDoc::get_DiscountSend
author: windows-sdk-content
description: Sets or retrieves the DiscountSend property for a FaxDoc object. The DiscountSend property is a Boolean value that indicates whether the fax server transmits faxes during the discount period.
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_discountsend_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_2usk.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: DiscountSend property [Fax Service], DiscountSend property [Fax Service],IFaxDoc interface, IFaxDoc interface [Fax Service],DiscountSend property, IFaxDoc.DiscountSend, IFaxDoc.get_DiscountSend, IFaxDoc::DiscountSend, IFaxDoc::get_DiscountSend, IFaxDoc::put_DiscountSend, _mfax_ifaxdoc_get_discountsend, fax._mfax_ifaxdoc_get_discountsend, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_discountsend_cpp, faxcom/IFaxDoc::DiscountSend, faxcom/IFaxDoc::get_DiscountSend, faxcom/IFaxDoc::put_DiscountSend, get_DiscountSend
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
 - IFaxDoc.DiscountSend
 - IFaxDoc.get_DiscountSend
 - IFaxDoc.put_DiscountSend
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
- IFaxDoc.get_DiscountSend
: 
---

# IFaxDoc::get_DiscountSend


## -description


Sets or retrieves the <b>DiscountSend</b> property for a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>DiscountSend</b> property is a Boolean value that indicates whether the fax server transmits faxes during the discount period.

This property is read/write.


## -parameters


## -remarks



To determine the period during which the discount rate applies, you can call the following <a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a> methods: <a href="https://msdn.microsoft.com/98355801-ad54-4b1e-a2f2-dcd22ede26e2">DiscountRateStartMinute</a>, <a href="https://msdn.microsoft.com/a8e1bf04-7fc4-48b3-8682-b06c550122a7">DiscountRateEndMinute</a>, <a href="https://msdn.microsoft.com/b144d4db-bd0e-4198-8653-6b22013c3d2e">DiscountRateStartHour</a>, and <a href="https://msdn.microsoft.com/959f2960-2e42-485e-9791-53849166bf88">DiscountRateEndHour</a>.




## -see-also




<a href="https://msdn.microsoft.com/959f2960-2e42-485e-9791-53849166bf88">DiscountRateEndHour</a>



<a href="https://msdn.microsoft.com/a8e1bf04-7fc4-48b3-8682-b06c550122a7">DiscountRateEndMinute</a>



<a href="https://msdn.microsoft.com/b144d4db-bd0e-4198-8653-6b22013c3d2e">DiscountRateStartHour</a>



<a href="https://msdn.microsoft.com/98355801-ad54-4b1e-a2f2-dcd22ede26e2">DiscountRateStartMinute</a>



<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/16f68004-fa4d-40c7-90a5-0bb562e72bd7">IFaxDoc</a>
 

 

