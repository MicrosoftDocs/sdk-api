---
UID: NF:faxcom.IFaxDoc.get_SenderDepartment
title: IFaxDoc::get_SenderDepartment
author: windows-sdk-content
description: Sets or retrieves the SenderDepartment property of a FaxDoc object. The SenderDepartment property is a null-terminated string that contains the department of the sender of the fax transmission.
old-location: fax\_mfax_ifaxdoc_get_senderdepartment_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0m7o.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: FaxDoc object [Fax Service],SenderDepartment property, FaxDoc.SenderDepartment, IFaxDoc.get_SenderDepartment, IFaxDoc::get_SenderDepartment, SenderDepartment property [Fax Service], SenderDepartment property [Fax Service],FaxDoc object, _mfax_ifaxdoc_get_senderdepartment, fax._mfax_ifaxdoc_get_senderdepartment, fax._mfax_ifaxdoc_get_senderdepartment_vb, get_SenderDepartment
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
 - FaxDoc.SenderDepartment
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDoc::get_SenderDepartment


## -description


Sets or retrieves the <b>SenderDepartment</b> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>SenderDepartment</b> property is a null-terminated string that contains the department of the sender of the fax transmission.

This property is read/write.


## -parameters


## -remarks



The fax sender's department can appear on the cover page.

The <b>get_SenderDepartment</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/6bf5be89-efc8-41e7-bde9-0c0ba7f0e61c">FaxDoc</a>



<a href="https://msdn.microsoft.com/16f68004-fa4d-40c7-90a5-0bb562e72bd7">IFaxDoc</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

