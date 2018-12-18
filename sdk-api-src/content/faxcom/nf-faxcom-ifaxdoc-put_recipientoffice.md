---
UID: NF:faxcom.IFaxDoc.put_RecipientOffice
title: IFaxDoc::put_RecipientOffice
author: windows-sdk-content
description: Sets or retrieves the RecipientOffice property of a FaxDoc object. The RecipientOffice property is a null-terminated string that contains the office of the recipient of the fax transmission.
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_recipientoffice_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_563p.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxDoc interface [Fax Service],RecipientOffice property, IFaxDoc.RecipientOffice, IFaxDoc.put_RecipientOffice, IFaxDoc::RecipientOffice, IFaxDoc::get_RecipientOffice, IFaxDoc::put_RecipientOffice, RecipientOffice property [Fax Service], RecipientOffice property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_recipientoffice, fax._mfax_ifaxdoc_get_recipientoffice, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipientoffice_cpp, faxcom/IFaxDoc::RecipientOffice, faxcom/IFaxDoc::get_RecipientOffice, faxcom/IFaxDoc::put_RecipientOffice, put_RecipientOffice
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
 - IFaxDoc.RecipientOffice
 - IFaxDoc.get_RecipientOffice
 - IFaxDoc.put_RecipientOffice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDoc::put_RecipientOffice


## -description


Sets or retrieves the <b>RecipientOffice</b> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientOffice</b> property is a null-terminated string that contains the office of the recipient of the fax transmission.

This property is read/write.


## -parameters


## -remarks



The fax recipient's office location can appear on the cover page.

The <b>get_RecipientOffice</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692281(v=VS.85).aspx">IFaxDoc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

