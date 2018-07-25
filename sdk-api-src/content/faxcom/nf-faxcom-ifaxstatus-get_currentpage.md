---
UID: NF:faxcom.IFaxStatus.get_CurrentPage
title: IFaxStatus::get_CurrentPage
author: windows-sdk-content
description: Retrieves the CurrentPage property for the FaxStatus object of a parent FaxPort object. The CurrentPage property is a number that identifies the current page of an active outbound fax job on a specific port.
old-location: fax\_mfax_ifaxstatus_get_currentpage_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3kx1.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: CurrentPage property [Fax Service], CurrentPage property [Fax Service],FaxStatus object, FaxStatus object [Fax Service],CurrentPage property, FaxStatus.CurrentPage, IFaxStatus.get_CurrentPage, IFaxStatus::get_CurrentPage, _mfax_ifaxstatus_get_currentpage, fax._mfax_ifaxstatus_get_currentpage, fax._mfax_ifaxstatus_get_currentpage_vb, get_CurrentPage
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
 - FaxStatus.CurrentPage
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxStatus::get_CurrentPage


## -description


Retrieves the <b>CurrentPage</b> property for the <a href="https://msdn.microsoft.com/library/ms691355(v=VS.85).aspx">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The <b>CurrentPage</b> property is a number that identifies the current page of an active outbound fax job on a specific port.

This property is read-only.


## -parameters


## -remarks



If the current page is not available, the <b>IFaxStatus::get_CurrentPage</b> method returns zero.

You can use the <b>CurrentPage</b> property of a <a href="https://msdn.microsoft.com/library/ms691355(v=VS.85).aspx">FaxStatus</a> object in conjunction with the <a href="https://msdn.microsoft.com/ae44f8d7-9447-425f-b7c4-fe0208205798">PageCount</a> property of the object to provide users with a running page count for an outbound fax job. For example, you could inform a user that the fax server is currently transmitting the second page of a four page transmission.




## -see-also




<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690310(v=VS.85).aspx">FaxStatus</a>



<a href="https://msdn.microsoft.com/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/library/ms690794(v=VS.85).aspx">IFaxStatus</a>



<a href="https://msdn.microsoft.com/ae44f8d7-9447-425f-b7c4-fe0208205798">PageCount</a>
 

 

