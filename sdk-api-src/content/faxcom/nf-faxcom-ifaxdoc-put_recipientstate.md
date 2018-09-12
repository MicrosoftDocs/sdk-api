---
UID: NF:faxcom.IFaxDoc.put_RecipientState
title: IFaxDoc::put_RecipientState
author: windows-sdk-content
description: Sets or retrieves the RecipientState property of a FaxDoc object. The RecipientState property is a null-terminated string that contains the state of the recipient of the fax transmission.
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_recipientstate_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3vqd.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IFaxDoc interface [Fax Service],RecipientState property, IFaxDoc.RecipientState, IFaxDoc.put_RecipientState, IFaxDoc::RecipientState, IFaxDoc::get_RecipientState, IFaxDoc::put_RecipientState, RecipientState property [Fax Service], RecipientState property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_recipientstate, fax._mfax_ifaxdoc_get_recipientstate, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipientstate_cpp, faxcom/IFaxDoc::RecipientState, faxcom/IFaxDoc::get_RecipientState, faxcom/IFaxDoc::put_RecipientState, put_RecipientState
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
 - IFaxDoc.RecipientState
 - IFaxDoc.get_RecipientState
 - IFaxDoc.put_RecipientState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDoc::put_RecipientState


## -description


Sets or retrieves the <b>RecipientState</b> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientState</b> property is a null-terminated string that contains the state of the recipient of the fax transmission.

This property is read/write.


## -parameters


## -remarks



The fax recipient's state name or state abbreviation can appear on the cover page.

The <b>get_RecipientState</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.



