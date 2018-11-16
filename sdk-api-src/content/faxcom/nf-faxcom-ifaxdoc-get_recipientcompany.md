---
UID: NF:faxcom.IFaxDoc.get_RecipientCompany
title: IFaxDoc::get_RecipientCompany
author: windows-sdk-content
description: Sets or retrieves the RecipientCompany property of a FaxDoc object. The RecipientCompany property is a null-terminated string that contains the company name of the recipient of the fax transmission.
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_recipientcompany_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0rjt.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFaxDoc interface [Fax Service],RecipientCompany property, IFaxDoc.RecipientCompany, IFaxDoc.get_RecipientCompany, IFaxDoc::RecipientCompany, IFaxDoc::get_RecipientCompany, IFaxDoc::put_RecipientCompany, RecipientCompany property [Fax Service], RecipientCompany property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_recipientcompany, fax._mfax_ifaxdoc_get_recipientcompany, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipientcompany_cpp, faxcom/IFaxDoc::RecipientCompany, faxcom/IFaxDoc::get_RecipientCompany, faxcom/IFaxDoc::put_RecipientCompany, get_RecipientCompany
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
 - IFaxDoc.RecipientCompany
 - IFaxDoc.get_RecipientCompany
 - IFaxDoc.put_RecipientCompany
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
- IFaxDoc.get_RecipientCompany
: 
---

# IFaxDoc::get_RecipientCompany


## -description


Sets or retrieves the <b>RecipientCompany</b> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientCompany</b> property is a null-terminated string that contains the company name of the recipient of the fax transmission.

This property is read/write.


## -parameters


## -remarks



The fax recipient's company name can appear on the cover page.

The <b>get_RecipientCompany</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692281(v=VS.85).aspx">IFaxDoc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

