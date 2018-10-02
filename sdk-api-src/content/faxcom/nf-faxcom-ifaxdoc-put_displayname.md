---
UID: NF:faxcom.IFaxDoc.put_DisplayName
title: IFaxDoc::put_DisplayName
author: windows-sdk-content
description: Sets or retrieves the DisplayName property of a FaxDoc object. The DisplayName property is a null-terminated string that contains the name to associate with the fax document.
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_displayname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_4s6d.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DisplayName property [Fax Service], DisplayName property [Fax Service],IFaxDoc interface, IFaxDoc interface [Fax Service],DisplayName property, IFaxDoc.DisplayName, IFaxDoc.put_DisplayName, IFaxDoc::DisplayName, IFaxDoc::get_DisplayName, IFaxDoc::put_DisplayName, _mfax_ifaxdoc_get_displayname, fax._mfax_ifaxdoc_get_displayname, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_displayname_cpp, faxcom/IFaxDoc::DisplayName, faxcom/IFaxDoc::get_DisplayName, faxcom/IFaxDoc::put_DisplayName, put_DisplayName
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
 - IFaxDoc.DisplayName
 - IFaxDoc.get_DisplayName
 - IFaxDoc.put_DisplayName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDoc::put_DisplayName


## -description


Sets or retrieves the <b>DisplayName</b> property of a <a href="https://msdn.microsoft.com/en-us/library/ms692317(v=VS.85).aspx">FaxDoc</a> object. The <b>DisplayName</b> property is a null-terminated string that contains the name to associate with the fax document.

This property is read/write.


## -parameters


## -remarks



The <b>get_DisplayName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692281(v=VS.85).aspx">IFaxDoc</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

