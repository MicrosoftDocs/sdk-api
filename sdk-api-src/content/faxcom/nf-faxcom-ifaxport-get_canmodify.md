---
UID: NF:faxcom.IFaxPort.get_CanModify
title: IFaxPort::get_CanModify
author: windows-sdk-content
description: The CanModify property is a Boolean value that indicates whether the user has permission to modify configuration information for the fax port.
old-location: fax\_mfax_ifaxport_get_canmodify_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_920p.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: CanModify property [Fax Service], CanModify property [Fax Service],FaxPort object, FaxPort object [Fax Service],CanModify property, FaxPort.CanModify, IFaxPort.get_CanModify, IFaxPort::get_CanModify, _mfax_ifaxport_get_canmodify, fax._mfax_ifaxport_get_canmodify, fax._mfax_ifaxport_get_canmodify_vb, get_CanModify
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
 - FaxPort.CanModify
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxPort::get_CanModify


## -description


The <b>CanModify</b> property is a Boolean value that indicates whether the user has permission to modify configuration information for the fax port.

This property is read-only.


## -parameters


## -remarks



To ensure that the client has permission to modify the specified fax port, a fax client application can call the <b>CanModify</b> property before calling any method that begins with <b>IFaxPort::put_</b>. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms691489(v=VS.85).aspx">Fax Device Management</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690315(v=VS.85).aspx">FaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>
 

 

