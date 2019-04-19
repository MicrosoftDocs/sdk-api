---
UID: NF:faxcom.IFaxDoc.get_RecipientDepartment
title: IFaxDoc::get_RecipientDepartment (faxcom.h)
author: windows-sdk-content
description: Sets or retrieves the RecipientDepartment property of a FaxDoc object. The RecipientDepartment property is a null-terminated string that contains the department of the recipient of the fax transmission.
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_recipientdepartment_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3mk4.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxDoc interface [Fax Service],RecipientDepartment property, IFaxDoc.RecipientDepartment, IFaxDoc.get_RecipientDepartment, IFaxDoc::RecipientDepartment, IFaxDoc::get_RecipientDepartment, IFaxDoc::put_RecipientDepartment, RecipientDepartment property [Fax Service], RecipientDepartment property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_recipientdepartment, fax._mfax_ifaxdoc_get_recipientdepartment, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipientdepartment_cpp, faxcom/IFaxDoc::RecipientDepartment, faxcom/IFaxDoc::get_RecipientDepartment, faxcom/IFaxDoc::put_RecipientDepartment, get_RecipientDepartment
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
 - IFaxDoc.RecipientDepartment
 - IFaxDoc.get_RecipientDepartment
 - IFaxDoc.put_RecipientDepartment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxDoc::get_RecipientDepartment


## -description


Sets or retrieves the <b>RecipientDepartment</b> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientDepartment</b> property is a null-terminated string that contains the department of the recipient of the fax transmission.

This property is read/write.


## -parameters


## -remarks



The sender's fax number can appear on the cover page.

The <b>get_RecipientDepartment</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692281(v=VS.85).aspx">IFaxDoc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

