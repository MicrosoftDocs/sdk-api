---
UID: NF:faxcom.IFaxDoc.get_RecipientState
title: IFaxDoc::get_RecipientState method
author: windows-driver-content
description: Sets or retrieves the RecipientState property of a FaxDoc object. The RecipientState property is a null-terminated string that contains the state of the recipient of the fax transmission.
old-location: fax\_mfax_ifaxdoc_get_recipientstate_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3vqd.htm
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: FaxDoc object [Fax Service], RecipientState property, IFaxDoc, IFaxDoc::get_RecipientState, RecipientState property [Fax Service], RecipientState property [Fax Service], FaxDoc object, _mfax_ifaxdoc_get_recipientstate, fax._mfax_ifaxdoc_get_recipientstate, fax._mfax_ifaxdoc_get_recipientstate_vb, get_RecipientState,IFaxDoc.get_RecipientState
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
req.typenames: ShellWindowTypeConstants
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Faxcom.dll
api_name:
-	FaxDoc.RecipientState
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDoc::get_RecipientState method


## -description


Sets or retrieves the <b>RecipientState</b> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>RecipientState</b> property is a null-terminated string that contains the state of the recipient of the fax transmission.

This property is read/write.


## -parameters


## -remarks



The fax recipient's state name or state abbreviation can appear on the cover page.

The <b>get_RecipientState</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.



