---
UID: NF:faxcom.IFaxStatus.get_SenderName
title: IFaxStatus::get_SenderName
author: windows-sdk-content
description: Retrieves the SenderName property for the FaxStatus object of a parent FaxPort object. The SenderName property is a null-terminated string that contains the name of the user who sent the fax transmission.
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_sendername_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_54x1.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFaxStatus interface [Fax Service],SenderName property, IFaxStatus.SenderName, IFaxStatus.get_SenderName, IFaxStatus::SenderName, IFaxStatus::get_SenderName, SenderName property [Fax Service], SenderName property [Fax Service],IFaxStatus interface, _mfax_ifaxstatus_get_sendername, fax._mfax_ifaxstatus_get_sendername, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_sendername_cpp, faxcom/IFaxStatus::SenderName, faxcom/IFaxStatus::get_SenderName, get_SenderName
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
 - IFaxStatus.SenderName
 - IFaxStatus.get_SenderName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcom.h
: 
- IFaxStatus.get_SenderName
: 
---

# IFaxStatus::get_SenderName


## -description


Retrieves the <b>SenderName</b> property for the <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The <b>SenderName</b> property is a null-terminated string that contains the name of the user who sent the fax transmission.

This property is read-only.


## -parameters


## -remarks



If the sender's name is not available, the <b>IFaxStatus::get_SenderName</b> method returns an empty string.

The <b>IFaxStatus::get_SenderName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690794(v=VS.85).aspx">IFaxStatus</a>



<a href="https://msdn.microsoft.com/239b98c5-be46-4e54-83f7-eb7f6250fa57">IFaxStatus::get_Send</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

