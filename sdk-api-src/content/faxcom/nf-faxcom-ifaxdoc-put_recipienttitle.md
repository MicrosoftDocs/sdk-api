---
UID: NF:faxcom.IFaxDoc.put_RecipientTitle
title: IFaxDoc::put_RecipientTitle
author: windows-sdk-content
description: Sets or retrieves the RecipientTitle property of a FaxDoc object. The RecipientTitle property is a null-terminated string that contains the title of the recipient of the fax transmission.
old-location: fax\_mfax_ifaxdoc_get_recipienttitle_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3bs5.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: FaxDoc object [Fax Service],RecipientTitle property, FaxDoc.RecipientTitle, IFaxDoc.put_RecipientTitle, IFaxDoc::put_RecipientTitle, RecipientTitle property [Fax Service], RecipientTitle property [Fax Service],FaxDoc object, _mfax_ifaxdoc_get_recipienttitle, fax._mfax_ifaxdoc_get_recipienttitle, fax._mfax_ifaxdoc_get_recipienttitle_vb, put_RecipientTitle
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
 - FaxDoc.RecipientTitle
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDoc::put_RecipientTitle


## -description


Sets or retrieves the <b>RecipientTitle</b> property of a <a href="https://msdn.microsoft.com/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>RecipientTitle</b> property is a null-terminated string that contains the title of the recipient of the fax transmission.

This property is read/write.


## -parameters


## -remarks



The sender's fax number can appear on the cover page.

The <a href="https://msdn.microsoft.com/e2d9bbbe-6878-4546-a2b9-be776dc18897">get_SenderFax</a> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690707(v=VS.85).aspx">FaxDoc</a>



<a href="https://msdn.microsoft.com/library/ms692281(v=VS.85).aspx">IFaxDoc</a>



<a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

