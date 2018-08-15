---
UID: NF:faxcom.IFaxDoc.put_SenderName
title: IFaxDoc::put_SenderName
author: windows-sdk-content
description: Sets or retrieves the SenderName property of a FaxDoc object. The SenderName property is a null-terminated string that contains the name of the sender of the fax transmission.
old-location: fax\_mfax_ifaxdoc_get_sendername_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_986d.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxDoc object [Fax Service],SenderName property, FaxDoc.SenderName, IFaxDoc.put_SenderName, IFaxDoc::put_SenderName, SenderName property [Fax Service], SenderName property [Fax Service],FaxDoc object, _mfax_ifaxdoc_get_sendername, fax._mfax_ifaxdoc_get_sendername, fax._mfax_ifaxdoc_get_sendername_vb, put_SenderName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: faxcom.h
req.include-header: 
req.redist: 
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
 - FaxDoc.SenderName
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDoc::put_SenderName


## -description


Sets or retrieves the <b>SenderName</b> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>SenderName</b> property is a null-terminated string that contains the name of the sender of the fax transmission.

This property is read/write.


## -parameters


## -remarks



The fax sender's name can appear on the cover page.

The <b>get_SenderName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690707(v=VS.85).aspx">FaxDoc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692281(v=VS.85).aspx">IFaxDoc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

