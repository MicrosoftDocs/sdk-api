---
UID: NF:faxcom.IFaxDoc.put_RecipientName
title: IFaxDoc::put_RecipientName
author: windows-sdk-content
description: Sets or retrieves the RecipientName property of a FaxDoc object. The RecipientName property is a null-terminated string that contains the name of the recipient of the fax transmission.
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_recipientname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5xut.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFaxDoc interface [Fax Service],RecipientName property, IFaxDoc.RecipientName, IFaxDoc.put_RecipientName, IFaxDoc::RecipientName, IFaxDoc::get_RecipientName, IFaxDoc::put_RecipientName, RecipientName property [Fax Service], RecipientName property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_recipientname, fax._mfax_ifaxdoc_get_recipientname, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipientname_cpp, faxcom/IFaxDoc::RecipientName, faxcom/IFaxDoc::get_RecipientName, faxcom/IFaxDoc::put_RecipientName, put_RecipientName
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

# IFaxDoc::put_RecipientName


## -description


Sets or retrieves the <b>RecipientName</b> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>RecipientName</b> property is a null-terminated string that contains the name of the recipient of the fax transmission.

This property is read/write.


## -parameters


## -remarks



The fax recipient's name can appear on the cover page.

The <b>get_RecipientName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/16f68004-fa4d-40c7-90a5-0bb562e72bd7">IFaxDoc</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

