---
UID: NF:faxcom.IFaxStatus.get_DeviceName
title: IFaxStatus::get_DeviceName
author: windows-sdk-content
description: Retrieves the DeviceName property for the FaxStatus object of a parent FaxPort object. The DeviceName property is a null-terminated string that contains the user-friendly display name for the fax port.
old-location: fax\_mfax_ifaxstatus_get_devicename_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_67mt.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: DeviceName property [Fax Service], DeviceName property [Fax Service],FaxStatus object, FaxStatus object [Fax Service],DeviceName property, FaxStatus.DeviceName, IFaxStatus.get_DeviceName, IFaxStatus::get_DeviceName, _mfax_ifaxstatus_get_devicename, fax._mfax_ifaxstatus_get_devicename, fax._mfax_ifaxstatus_get_devicename_vb, get_DeviceName
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
 - FaxStatus.DeviceName
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxStatus::get_DeviceName


## -description


Retrieves the <b>DeviceName</b> property for the <a href="https://msdn.microsoft.com/library/ms691355(v=VS.85).aspx">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The <b>DeviceName</b> property is a null-terminated string that contains the user-friendly display name for the fax port.

This property is read-only.


## -parameters


## -remarks



Note that it is possible for multiple fax ports to have the same user-friendly name. You can use the <a href="https://msdn.microsoft.com/14139556-eac3-41b8-9fc9-cb1eb6ffca8f">DeviceId</a> property of a <a href="https://msdn.microsoft.com/library/ms691355(v=VS.85).aspx">FaxStatus</a> object to uniquely identify a fax port, and associate a FaxStatus object with a <a href="https://msdn.microsoft.com/library/ms691338(v=VS.85).aspx">FaxPort</a> object.

The <b>IFaxStatus::get_DeviceName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/14139556-eac3-41b8-9fc9-cb1eb6ffca8f">DeviceId</a>



<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690310(v=VS.85).aspx">FaxStatus</a>



<a href="https://msdn.microsoft.com/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/library/ms690794(v=VS.85).aspx">IFaxStatus</a>



<a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

