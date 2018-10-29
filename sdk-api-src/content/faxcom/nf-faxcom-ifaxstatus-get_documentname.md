---
UID: NF:faxcom.IFaxStatus.get_DocumentName
title: IFaxStatus::get_DocumentName
author: windows-sdk-content
description: Retrieves the DocumentName property for the FaxStatus object of a parent FaxPort object. The DocumentName property is a null-terminated string that contains the user-friendly name associated with an active fax document.
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_documentname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6jvp.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: DocumentName property [Fax Service], DocumentName property [Fax Service],IFaxStatus interface, IFaxStatus interface [Fax Service],DocumentName property, IFaxStatus.DocumentName, IFaxStatus.get_DocumentName, IFaxStatus::DocumentName, IFaxStatus::get_DocumentName, _mfax_ifaxstatus_get_documentname, fax._mfax_ifaxstatus_get_documentname, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_documentname_cpp, faxcom/IFaxStatus::DocumentName, faxcom/IFaxStatus::get_DocumentName, get_DocumentName
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
 - IFaxStatus.DocumentName
 - IFaxStatus.get_DocumentName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxStatus::get_DocumentName


## -description


Retrieves the <b>DocumentName</b> property for the <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The <b>DocumentName</b> property is a null-terminated string that contains the user-friendly name associated with an active fax document.

This property is read-only.


## -parameters


## -remarks



You can use the <b>DocumentName</b> property of a <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object in conjunction with the <a href="https://msdn.microsoft.com/ec9b9196-f937-4601-b7a8-d5f2a33b276e">DocumentSize</a> property of the object to inform users about the size of outbound jobs. 

The <b>IFaxStatus::get_DocumentName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690794(v=VS.85).aspx">IFaxStatus</a>



<a href="https://msdn.microsoft.com/ec9b9196-f937-4601-b7a8-d5f2a33b276e">IFaxStatus::get_DocumentSize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

