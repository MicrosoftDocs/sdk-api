---
UID: NF:faxcom.IFaxDoc.get_RecipientName
title: IFaxDoc::get_RecipientName
author: windows-sdk-content
description: Sets or retrieves the RecipientName property of a FaxDoc object. The RecipientName property is a null-terminated string that contains the name of the recipient of the fax transmission.
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_recipientname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5xut.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxDoc interface [Fax Service],RecipientName property, IFaxDoc.RecipientName, IFaxDoc.get_RecipientName, IFaxDoc::RecipientName, IFaxDoc::get_RecipientName, IFaxDoc::put_RecipientName, RecipientName property [Fax Service], RecipientName property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_recipientname, fax._mfax_ifaxdoc_get_recipientname, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipientname_cpp, faxcom/IFaxDoc::RecipientName, faxcom/IFaxDoc::get_RecipientName, faxcom/IFaxDoc::put_RecipientName, get_RecipientName
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
 - IFaxDoc.RecipientName
 - IFaxDoc.get_RecipientName
 - IFaxDoc.put_RecipientName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDoc::get_RecipientName


## -description


Sets or retrieves the <b>RecipientName</b> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientName</b> property is a null-terminated string that contains the name of the recipient of the fax transmission.

This property is read/write.


## -parameters


## -remarks



The fax recipient's name can appear on the cover page.

The <b>get_RecipientName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692281(v=VS.85).aspx">IFaxDoc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

