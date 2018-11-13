---
UID: NF:faxcom.IFaxStatus.get_PageCount
title: IFaxStatus::get_PageCount
author: windows-sdk-content
description: Retrieves the PageCount property for the FaxStatus object of a parent FaxPort object. The PageCount property represents the total number of pages in an outbound fax transmission.
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_pagecount_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6xv8.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxStatus interface [Fax Service],PageCount property, IFaxStatus.PageCount, IFaxStatus.get_PageCount, IFaxStatus::PageCount, IFaxStatus::get_PageCount, PageCount property [Fax Service], PageCount property [Fax Service],IFaxStatus interface, _mfax_ifaxstatus_get_pagecount, fax._mfax_ifaxstatus_get_pagecount, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_pagecount_cpp, faxcom/IFaxStatus::PageCount, faxcom/IFaxStatus::get_PageCount, get_PageCount
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
 - IFaxStatus.PageCount
 - IFaxStatus.get_PageCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxStatus::get_PageCount


## -description


Retrieves the <b>PageCount</b> property for the <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The <b>PageCount</b> property represents the total number of pages in an outbound fax transmission.

This property is read-only.


## -parameters


## -remarks



If the page count is not available, the <b>IFaxStatus::get_PageCount</b> method returns zero.

You can use the <b>PageCount</b> property of a <a href="https://msdn.microsoft.com/en-us/library/ms691355(v=VS.85).aspx">FaxStatus</a> object in conjunction with the <a href="https://msdn.microsoft.com/a0916ecc-7800-4a13-bcc1-9212b07d35e3">CurrentPage</a> property of the object to provide users with a running page count for an outbound fax job. For example, you could inform a user that the fax server is currently transmitting the second page of a four page transmission.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690794(v=VS.85).aspx">IFaxStatus</a>



<a href="https://msdn.microsoft.com/a0916ecc-7800-4a13-bcc1-9212b07d35e3">IFaxStatus::get_CurrentPage</a>
 

 

