---
UID: NF:faxcom.IFaxDoc.put_RecipientHomePhone
title: IFaxDoc::put_RecipientHomePhone
author: windows-sdk-content
description: Sets or retrieves the RecipientHomePhone property of a FaxDoc object. The RecipientHomePhone property is a null-terminated string that contains the home telephone number of the recipient of the fax transmission.
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_recipienthomephone_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9m5h.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxDoc interface [Fax Service],RecipientHomePhone property, IFaxDoc.RecipientHomePhone, IFaxDoc.put_RecipientHomePhone, IFaxDoc::RecipientHomePhone, IFaxDoc::get_RecipientHomePhone, IFaxDoc::put_RecipientHomePhone, RecipientHomePhone property [Fax Service], RecipientHomePhone property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_recipienthomephone, fax._mfax_ifaxdoc_get_recipienthomephone, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipienthomephone_cpp, faxcom/IFaxDoc::RecipientHomePhone, faxcom/IFaxDoc::get_RecipientHomePhone, faxcom/IFaxDoc::put_RecipientHomePhone, put_RecipientHomePhone
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
 - IFaxDoc.RecipientHomePhone
 - IFaxDoc.get_RecipientHomePhone
 - IFaxDoc.put_RecipientHomePhone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDoc::put_RecipientHomePhone


## -description


Sets or retrieves the <b>RecipientHomePhone</b> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientHomePhone</b> property is a null-terminated string that contains the home telephone number of the recipient of the fax transmission.

This property is read/write.


## -parameters


## -remarks



The fax recipient's home telephone number can appear on the cover page.

The <b>get_RecipientHomePhone</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692281(v=VS.85).aspx">IFaxDoc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

