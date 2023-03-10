---
UID: NF:faxcom.IFaxDoc.get_RecipientState
title: IFaxDoc::get_RecipientState (faxcom.h)
description: Sets or retrieves the RecipientState property of a FaxDoc object. The RecipientState property is a null-terminated string that contains the state of the recipient of the fax transmission. (Get)
helpviewer_keywords: ["IFaxDoc interface [Fax Service]","RecipientState property","IFaxDoc.RecipientState","IFaxDoc.get_RecipientState","IFaxDoc::RecipientState","IFaxDoc::get_RecipientState","IFaxDoc::put_RecipientState","RecipientState property [Fax Service]","RecipientState property [Fax Service]","IFaxDoc interface","_mfax_ifaxdoc_get_recipientstate","fax._mfax_ifaxdoc_get_recipientstate","fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipientstate_cpp","faxcom/IFaxDoc::RecipientState","faxcom/IFaxDoc::get_RecipientState","faxcom/IFaxDoc::put_RecipientState","get_RecipientState"]
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_recipientstate_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3vqd.htm
ms.date: 12/05/2018
ms.keywords: IFaxDoc interface [Fax Service],RecipientState property, IFaxDoc.RecipientState, IFaxDoc.get_RecipientState, IFaxDoc::RecipientState, IFaxDoc::get_RecipientState, IFaxDoc::put_RecipientState, RecipientState property [Fax Service], RecipientState property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_recipientstate, fax._mfax_ifaxdoc_get_recipientstate, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_recipientstate_cpp, faxcom/IFaxDoc::RecipientState, faxcom/IFaxDoc::get_RecipientState, faxcom/IFaxDoc::put_RecipientState, get_RecipientState
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxDoc::get_RecipientState
 - faxcom/IFaxDoc::get_RecipientState
dev_langs:
 - c++
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
---

# IFaxDoc::get_RecipientState


## -description

Sets or retrieves the <b>RecipientState</b> property of a <a href="/previous-versions/windows/desktop/fax/-mfax-faxdoc">FaxDoc</a> object. The <b>RecipientState</b> property is a null-terminated string that contains the state of the recipient of the fax transmission.

This property is read/write.

## -parameters

## -remarks

The fax recipient's state name or state abbreviation can appear on the cover page.

The <b>get_RecipientState</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.
