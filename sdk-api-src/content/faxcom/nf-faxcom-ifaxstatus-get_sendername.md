---
UID: NF:faxcom.IFaxStatus.get_SenderName
title: IFaxStatus::get_SenderName
author: windows-sdk-content
description: Retrieves the SenderName property for the FaxStatus object of a parent FaxPort object. The SenderName property is a null-terminated string that contains the name of the user who sent the fax transmission.
old-location: fax\_mfax_ifaxstatus_get_sendername_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_54x1.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FaxStatus object [Fax Service],SenderName property, FaxStatus.SenderName, IFaxStatus.get_SenderName, IFaxStatus::get_SenderName, SenderName property [Fax Service], SenderName property [Fax Service],FaxStatus object, _mfax_ifaxstatus_get_sendername, fax._mfax_ifaxstatus_get_sendername, fax._mfax_ifaxstatus_get_sendername_vb, get_SenderName
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
 - FaxStatus.SenderName
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxStatus::get_SenderName


## -description


Retrieves the <b>SenderName</b> property for the <a href="https://msdn.microsoft.com/library/ms691355(v=VS.85).aspx">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The <b>SenderName</b> property is a null-terminated string that contains the name of the user who sent the fax transmission.

This property is read-only.


## -parameters


## -remarks



If the sender's name is not available, the <b>IFaxStatus::get_SenderName</b> method returns an empty string.

The <b>IFaxStatus::get_SenderName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690310(v=VS.85).aspx">FaxStatus</a>



<a href="https://msdn.microsoft.com/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/library/ms690794(v=VS.85).aspx">IFaxStatus</a>



<a href="https://msdn.microsoft.com/e7759c8a-a6f3-4e42-9d56-bf93d11d7ad1">Send</a>



<a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

