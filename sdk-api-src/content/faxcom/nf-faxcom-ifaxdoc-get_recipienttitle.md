---
UID: NF:faxcom.IFaxDoc.get_RecipientTitle
title: IFaxDoc::get_RecipientTitle
author: windows-sdk-content
description: Sets or retrieves the RecipientTitle property of a FaxDoc object. The RecipientTitle property is a null-terminated string that contains the title of the recipient of the fax transmission.
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_recipienttitle_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3bs5.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxDoc interface [Fax Service],RecipientTitle property, IFaxDoc.RecipientTitle, IFaxDoc.get_RecipientTitle, IFaxDoc::RecipientTitle, IFaxDoc::get_RecipientTitle, IFaxDoc::put_RecipientTitle, RecipientTitle property [Fax Service], RecipientTitle property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_recipienttitle, fax._mfax_ifaxdoc_get_recipienttitle, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipienttitle_cpp, faxcom/IFaxDoc::RecipientTitle, faxcom/IFaxDoc::get_RecipientTitle, faxcom/IFaxDoc::put_RecipientTitle, get_RecipientTitle
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
 - IFaxDoc.RecipientTitle
 - IFaxDoc.get_RecipientTitle
 - IFaxDoc.put_RecipientTitle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDoc::get_RecipientTitle


## -description


Sets or retrieves the <b>RecipientTitle</b> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientTitle</b> property is a null-terminated string that contains the title of the recipient of the fax transmission.

This property is read/write.


## -parameters


## -remarks



The sender's fax number can appear on the cover page.

The <a href="https://msdn.microsoft.com/a884bcf2-5769-45d7-b112-6550e57e52ed">get_SenderFax</a> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692281(v=VS.85).aspx">IFaxDoc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

