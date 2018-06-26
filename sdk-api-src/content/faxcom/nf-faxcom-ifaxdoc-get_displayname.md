---
UID: NF:faxcom.IFaxDoc.get_DisplayName
title: IFaxDoc::get_DisplayName
author: windows-sdk-content
description: Sets or retrieves the DisplayName property of a FaxDoc object. The DisplayName property is a null-terminated string that contains the name to associate with the fax document.
old-location: fax\_mfax_ifaxdoc_get_displayname_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_4s6d.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: DisplayName property [Fax Service], DisplayName property [Fax Service],FaxDoc object, FaxDoc object [Fax Service],DisplayName property, FaxDoc.DisplayName, IFaxDoc.get_DisplayName, IFaxDoc::get_DisplayName, _mfax_ifaxdoc_get_displayname, fax._mfax_ifaxdoc_get_displayname, fax._mfax_ifaxdoc_get_displayname_vb, get_DisplayName
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
 - FaxDoc.DisplayName
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxDoc::get_DisplayName


## -description


Sets or retrieves the <b>DisplayName</b> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>DisplayName</b> property is a null-terminated string that contains the name to associate with the fax document.

This property is read/write.


## -parameters


## -remarks



The <b>get_DisplayName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/6bf5be89-efc8-41e7-bde9-0c0ba7f0e61c">FaxDoc</a>



<a href="https://msdn.microsoft.com/16f68004-fa4d-40c7-90a5-0bb562e72bd7">IFaxDoc</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

