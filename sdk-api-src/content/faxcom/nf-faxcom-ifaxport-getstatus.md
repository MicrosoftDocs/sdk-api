---
UID: NF:faxcom.IFaxPort.GetStatus
title: IFaxPort::GetStatus
author: windows-sdk-content
description: The GetStatus method creates a FaxStatus object for the parent FaxPort object. The FaxStatus object contains the current status of a fax port.
old-location: fax\_mfax_ifaxport_getstatus_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8lo3.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxPort object [Fax Service],GetStatus method, FaxPort.GetStatus, GetStatus, GetStatus method [Fax Service], GetStatus method [Fax Service],FaxPort object, IFaxPort.GetStatus, IFaxPort::GetStatus, _mfax_ifaxport_getstatus, fax._mfax_ifaxport_getstatus, fax._mfax_ifaxport_getstatus_vb
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
 - FaxPort.GetStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxPort::GetStatus


## -description


The <b>GetStatus</b> method creates a <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object for the parent <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The FaxStatus object contains the current status of a fax port.


## -parameters




### -param retval






#### - retVal [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>*</b>

Retrieves a <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object.


## -remarks



The <b>GetStatus</b> method retrieves an <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object. A fax client application can also access the <a href="https://msdn.microsoft.com/en-us/library/ms690794(v=VS.85).aspx">IFaxStatus</a> interface directly by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxStatus</b> interface pointer.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690315(v=VS.85).aspx">FaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690794(v=VS.85).aspx">IFaxStatus</a>
 

 

