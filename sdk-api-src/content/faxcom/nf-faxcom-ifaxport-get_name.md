---
UID: NF:faxcom.IFaxPort.get_Name
title: IFaxPort::get_Name
author: windows-sdk-content
description: The Name property is a null-terminated string that contains the user-friendly display name for a fax port.
old-location: fax\_mfax_ifaxport_get_name_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1ep1.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FaxPort object [Fax Service],Name property, FaxPort.Name, IFaxPort.get_Name, IFaxPort::get_Name, Name property [Fax Service], Name property [Fax Service],FaxPort object, _mfax_ifaxport_get_name, fax._mfax_ifaxport_get_name, fax._mfax_ifaxport_get_name_vb, get_Name
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
 - FaxPort.Name
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxPort::get_Name


## -description


The <b>Name</b> property is a null-terminated string that contains the 
user-friendly display name for a fax port.

This property is read-only.


## -parameters


## -remarks



Note that it is possible for multiple fax ports to have the same user-friendly 
name. Use the <a href="https://msdn.microsoft.com/f7720dda-3635-4a23-9dc4-09cac4b6aa17">DeviceId</a> property to uniquely identify a fax port.

<b>Name</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f7720dda-3635-4a23-9dc4-09cac4b6aa17">DeviceId</a>



<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690315(v=VS.85).aspx">FaxPort</a>



<a href="https://msdn.microsoft.com/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/library/ms690893(v=VS.85).aspx">IFaxPorts</a>
 

 

