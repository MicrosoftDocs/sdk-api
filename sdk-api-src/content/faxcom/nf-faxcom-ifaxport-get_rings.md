---
UID: NF:faxcom.IFaxPort.get_Rings
title: IFaxPort::get_Rings
author: windows-sdk-content
description: The Rings property represents the number of rings an incoming fax call should wait before the fax port answers the call.
old-location: fax\_mfax_ifaxport_get_rings_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3jjn.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FaxPort object [Fax Service],Rings property, FaxPort.Rings, IFaxPort.get_Rings, IFaxPort::get_Rings, Rings property [Fax Service], Rings property [Fax Service],FaxPort object, _mfax_ifaxport_get_rings, fax._mfax_ifaxport_get_rings, fax._mfax_ifaxport_get_rings_vb, get_Rings
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
 - FaxPort.Rings
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxPort::get_Rings


## -description


The <b>Rings</b> property represents the number of rings an incoming fax call should wait before the fax port answers the call. 

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  Before setting a value for this property, a fax client application can call the <a href="https://msdn.microsoft.com/en-us/library/ms692798(v=VS.85).aspx">CanModify</a> property to ensure that the client has permission to modify configuration information for the specified fax port.</div>
<div> </div>
The fax server ignores the <b>Rings</b> property unless the specified fax port is enabled to receive faxes.




## -see-also




<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690315(v=VS.85).aspx">FaxPort</a>



<a href="https://msdn.microsoft.com/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/library/ms690893(v=VS.85).aspx">IFaxPorts</a>
 

 

