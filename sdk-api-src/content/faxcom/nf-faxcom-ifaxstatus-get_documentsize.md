---
UID: NF:faxcom.IFaxStatus.get_DocumentSize
title: IFaxStatus::get_DocumentSize (faxcom.h)
author: windows-sdk-content
description: Retrieves the DocumentSize property for the FaxStatus object of a parent FaxPort object. The DocumentSize property is the size of the fax document associated with the active outbound job on a specific port.
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_documentsize_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5d5x.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DocumentSize property [Fax Service], DocumentSize property [Fax Service],IFaxStatus interface, IFaxStatus interface [Fax Service],DocumentSize property, IFaxStatus.DocumentSize, IFaxStatus.get_DocumentSize, IFaxStatus::DocumentSize, IFaxStatus::get_DocumentSize, _mfax_ifaxstatus_get_documentsize, fax._mfax_ifaxstatus_get_documentsize, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_documentsize_cpp, faxcom/IFaxStatus::DocumentSize, faxcom/IFaxStatus::get_DocumentSize, get_DocumentSize
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
 - IFaxStatus.DocumentSize
 - IFaxStatus.get_DocumentSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxStatus::get_DocumentSize


## -description


Retrieves the <b>DocumentSize</b> property for the <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The <b>DocumentSize</b> property is the size of the fax document associated with the active outbound job on a specific port.

This property is read-only.


## -parameters


## -remarks



You can use the <b>DocumentSize</b> property of a <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object in conjunction with the <a href="https://msdn.microsoft.com/en-us/library/ms691962(v=VS.85).aspx">DocumentName</a> property of the object to inform users about the size of outbound jobs.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690794(v=VS.85).aspx">IFaxStatus</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691962(v=VS.85).aspx">IFaxStatus::get_DocumentName</a>
 

 

