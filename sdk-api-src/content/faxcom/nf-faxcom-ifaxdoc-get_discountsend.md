---
UID: NF:faxcom.IFaxDoc.get_DiscountSend
title: IFaxDoc::get_DiscountSend
author: windows-sdk-content
description: Sets or retrieves the DiscountSend property for a FaxDoc object. The DiscountSend property is a Boolean value that indicates whether the fax server transmits faxes during the discount period.
old-location: fax\_mfax_ifaxdoc_get_discountsend_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_2usk.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
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


Sets or retrieves the <b>DiscountSend</b> property for a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>DiscountSend</b> property is a Boolean value that indicates whether the fax server transmits faxes during the discount period.

This property is read/write.


## -parameters


## -remarks



To determine the period during which the discount rate applies, you can call the following <a href="https://msdn.microsoft.com/f06b76b5-b6c2-47a0-ad08-7c1bf7b780bb">IFaxServer</a> methods: <a href="https://msdn.microsoft.com/5159eb01-d464-4cc3-8617-e785c97ff6ff">DiscountRateStartMinute</a>, <a href="https://msdn.microsoft.com/db9e206b-d398-4924-93b9-c7628043dd23">DiscountRateEndMinute</a>, <a href="https://msdn.microsoft.com/1ba6f885-08a2-4ee5-9120-c9da3e01c570">DiscountRateStartHour</a>, and <a href="https://msdn.microsoft.com/a953c003-3a0c-4d75-a86f-6397ce776c2f">DiscountRateEndHour</a>.




## -see-also




<a href="https://msdn.microsoft.com/a953c003-3a0c-4d75-a86f-6397ce776c2f">DiscountRateEndHour</a>



<a href="https://msdn.microsoft.com/db9e206b-d398-4924-93b9-c7628043dd23">DiscountRateEndMinute</a>



<a href="https://msdn.microsoft.com/1ba6f885-08a2-4ee5-9120-c9da3e01c570">DiscountRateStartHour</a>



<a href="https://msdn.microsoft.com/5159eb01-d464-4cc3-8617-e785c97ff6ff">DiscountRateStartMinute</a>



<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/6bf5be89-efc8-41e7-bde9-0c0ba7f0e61c">FaxDoc</a>



<a href="https://msdn.microsoft.com/16f68004-fa4d-40c7-90a5-0bb562e72bd7">IFaxDoc</a>
 

 

