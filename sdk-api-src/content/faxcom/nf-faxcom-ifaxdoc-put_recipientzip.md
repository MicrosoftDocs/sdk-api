---
UID: NF:faxcom.IFaxDoc.put_RecipientZip
title: IFaxDoc::put_RecipientZip
author: windows-sdk-content
description: Sets or retrieves the RecipientZip property of a FaxDoc object. The RecipientZip property is a null-terminated string that contains the ZIP code of the recipient of the fax transmission.
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_recipientzip_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_2pww.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxDoc interface [Fax Service],RecipientZip property, IFaxDoc.RecipientZip, IFaxDoc.put_RecipientZip, IFaxDoc::RecipientZip, IFaxDoc::get_RecipientZip, IFaxDoc::put_RecipientZip, RecipientZip property [Fax Service], RecipientZip property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_recipientzip, fax._mfax_ifaxdoc_get_recipientzip, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipientzip_cpp, faxcom/IFaxDoc::RecipientZip, faxcom/IFaxDoc::get_RecipientZip, faxcom/IFaxDoc::put_RecipientZip, put_RecipientZip
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
 - IFaxDoc.RecipientZip
 - IFaxDoc.get_RecipientZip
 - IFaxDoc.put_RecipientZip
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
- IFaxDoc.put_RecipientZip
: 
---

# IFaxDoc::put_RecipientZip


## -description


Sets or retrieves the <b>RecipientZip</b> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>RecipientZip</b> property is a null-terminated string that contains the ZIP code of the recipient of the fax transmission.

This property is read/write.


## -parameters


## -remarks



The fax recipient's postal ZIP code can appear on the cover page.

The <b>get_RecipientZip</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/16f68004-fa4d-40c7-90a5-0bb562e72bd7">IFaxDoc</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

