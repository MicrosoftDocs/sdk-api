---
UID: NF:faxcom.IFaxDoc.put_SenderFax
title: IFaxDoc::put_SenderFax
author: windows-sdk-content
description: Sets or retrieves the SenderFax property of a FaxDoc object. The SenderFax property is a null-terminated string that contains the fax number of the sender of the outbound fax transmission.
old-location: fax\_mfax_ifaxdoc_get_senderfax_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_02ew.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: FaxDoc object [Fax Service],SenderFax property, FaxDoc.SenderFax, IFaxDoc.put_SenderFax, IFaxDoc::put_SenderFax, SenderFax property [Fax Service], SenderFax property [Fax Service],FaxDoc object, _mfax_ifaxdoc_get_senderfax, fax._mfax_ifaxdoc_get_senderfax, fax._mfax_ifaxdoc_get_senderfax_vb, put_SenderFax
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
 - FaxDoc.SenderFax
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDoc::put_SenderFax


## -description


Sets or retrieves the <b>SenderFax</b> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>SenderFax</b> property is a null-terminated string that contains the fax number of the sender of the outbound fax transmission.

This property is read/write.


## -parameters


## -remarks



The sender's fax number can appear on the cover page.

The <b>get_SenderFax</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/6bf5be89-efc8-41e7-bde9-0c0ba7f0e61c">FaxDoc</a>



<a href="https://msdn.microsoft.com/16f68004-fa4d-40c7-90a5-0bb562e72bd7">IFaxDoc</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

