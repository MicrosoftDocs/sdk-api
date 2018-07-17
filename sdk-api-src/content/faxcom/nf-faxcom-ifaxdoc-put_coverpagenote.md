---
UID: NF:faxcom.IFaxDoc.put_CoverpageNote
title: IFaxDoc::put_CoverpageNote
author: windows-sdk-content
description: Sets or retrieves the CoverpageNote property of a FaxDoc object. The CoverpageNote property is a null-terminated string that contains the text of a message or note from the sender that pertains to the fax transmission.
old-location: fax\_mfax_ifaxdoc_get_coverpagenote_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_4t7p.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: CoverpageNote property [Fax Service], CoverpageNote property [Fax Service],FaxDoc object, FaxDoc object [Fax Service],CoverpageNote property, FaxDoc.CoverpageNote, IFaxDoc.put_CoverpageNote, IFaxDoc::put_CoverpageNote, _mfax_ifaxdoc_get_coverpagenote, fax._mfax_ifaxdoc_get_coverpagenote, fax._mfax_ifaxdoc_get_coverpagenote_vb, put_CoverpageNote
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
 - FaxDoc.CoverpageNote
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDoc::put_CoverpageNote


## -description


Sets or retrieves the <b>CoverpageNote</b> property of a <a href="https://msdn.microsoft.com/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>CoverpageNote</b> property is a null-terminated string that contains the text of a message or note from the sender that pertains to the fax transmission.

This property is read/write.


## -parameters


## -remarks



The cover page note can appear on the cover page.

The <b>get_CoverpageNote</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690707(v=VS.85).aspx">FaxDoc</a>



<a href="https://msdn.microsoft.com/library/ms692281(v=VS.85).aspx">IFaxDoc</a>



<a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

