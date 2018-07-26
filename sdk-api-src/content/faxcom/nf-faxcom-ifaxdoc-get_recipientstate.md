---
UID: NF:faxcom.IFaxDoc.get_RecipientState
title: IFaxDoc::get_RecipientState
author: windows-sdk-content
description: Sets or retrieves the RecipientState property of a FaxDoc object. The RecipientState property is a null-terminated string that contains the state of the recipient of the fax transmission.
old-location: fax\_mfax_ifaxdoc_get_recipientstate_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3vqd.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FaxDoc object [Fax Service],RecipientState property, FaxDoc.RecipientState, IFaxDoc.get_RecipientState, IFaxDoc::get_RecipientState, RecipientState property [Fax Service], RecipientState property [Fax Service],FaxDoc object, _mfax_ifaxdoc_get_recipientstate, fax._mfax_ifaxdoc_get_recipientstate, fax._mfax_ifaxdoc_get_recipientstate_vb, get_RecipientState
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ShellWindowTypeConstants
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - FaxDoc.RecipientState
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDoc::get_RecipientState


## -description


Sets or retrieves the <b>RecipientState</b> property of a <a href="https://msdn.microsoft.com/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientState</b> property is a null-terminated string that contains the state of the recipient of the fax transmission.

This property is read/write.


## -parameters


## -remarks



The fax recipient's state name or state abbreviation can appear on the cover page.

The <b>get_RecipientState</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.



