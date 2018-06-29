---
UID: NF:faxcom.IFaxDoc.get_BillingCode
title: IFaxDoc::get_BillingCode
author: windows-sdk-content
description: Sets or retrieves the BillingCode property of a FaxDoc object. The BillingCode property is a null-terminated string that contains an optional billing code that applies to the fax transmission.
old-location: fax\_mfax_ifaxdoc_get_billingcode_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_95yd.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: BillingCode property [Fax Service], BillingCode property [Fax Service],FaxDoc object, FaxDoc object [Fax Service],BillingCode property, FaxDoc.BillingCode, IFaxDoc.get_BillingCode, IFaxDoc::get_BillingCode, _mfax_ifaxdoc_get_billingcode, fax._mfax_ifaxdoc_get_billingcode, fax._mfax_ifaxdoc_get_billingcode_vb, get_BillingCode
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
 - FaxDoc.BillingCode
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDoc::get_BillingCode


## -description


Sets or retrieves the <b>BillingCode</b> property of a <a href="https://msdn.microsoft.com/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>BillingCode</b> property is a null-terminated string that contains an optional billing code that applies to the fax transmission.

This property is read/write.


## -parameters


## -remarks



The fax server uses the <b>BillingCode</b> property to generate an entry in the fax event log. Billing codes are optional.

The <b>get_BillingCode</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690707(v=VS.85).aspx">FaxDoc</a>



<a href="https://msdn.microsoft.com/library/ms692281(v=VS.85).aspx">IFaxDoc</a>



<a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

