---
UID: NF:faxcom.IFaxTiff.get_ReceiveTime
title: IFaxTiff::get_ReceiveTime
author: windows-sdk-content
description: Retrieves the ReceiveTime property for a FaxTiff object.
old-location: fax\_mfax_ifaxtiff_mfax_ifaxtiff_get_receivetime_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5spx.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: IFaxTiff interface [Fax Service],ReceiveTime property, IFaxTiff.ReceiveTime, IFaxTiff.get_ReceiveTime, IFaxTiff::ReceiveTime, IFaxTiff::get_ReceiveTime, ReceiveTime property [Fax Service], ReceiveTime property [Fax Service],IFaxTiff interface, _mfax_ifaxtiff_get_receivetime, fax._mfax_ifaxtiff_get_receivetime, fax._mfax_ifaxtiff_mfax_ifaxtiff_get_receivetime_cpp, faxcom/IFaxTiff::ReceiveTime, faxcom/IFaxTiff::get_ReceiveTime, get_ReceiveTime
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
 - IFaxTiff.ReceiveTime
 - IFaxTiff.get_ReceiveTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxTiff::get_ReceiveTime


## -description


Retrieves the <b>ReceiveTime</b> property for a <a href="https://msdn.microsoft.com/en-us/library/ms691832(v=VS.85).aspx">FaxTiff</a> object. The <b>ReceiveTime</b> property is a null-terminated string that contains the time at which reception began for an inbound fax file. The string can contain the time at which reception or transmission began for an archived file.

This property is read-only.


## -parameters


## -remarks



A fax client application must  set the <a href="https://msdn.microsoft.com/c993c276-eb77-4173-bfc5-0c82decb2b52">Image</a> property before retrieving another property for a <a href="https://msdn.microsoft.com/en-us/library/ms691832(v=VS.85).aspx">FaxTiff</a> object.

The <b>get_ReceiveTime</b> method sets the <i>pVal</i> parameter to the time at which reception began for an inbound fax file, if it is available. If the information is not available, the method returns an empty string.

The <b>ReceiveTime</b> property is a string that represents the time at which reception began for an inbound fax file, if it is available. If the information is not available, <b>RecipientName</b> is "Unavailable".

The <b>get_ReceiveTime</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.

The fax service formats the string according to the user's locale. It is a concatenation of the date and time the service transmitted the fax. The date is separated from the time by an "@" character. For example, in the English locale, a string would be formatted as follows:

10/02/98@10:15AM

The <a href="https://msdn.microsoft.com/1bc248b7-a8ff-430a-9ab7-1bad9186696c">RawReceiveTime</a> property contains the time expressed in Coordinated Universal Time (UTC).




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691802(v=VS.85).aspx">IFaxTiff</a>



<a href="https://msdn.microsoft.com/c993c276-eb77-4173-bfc5-0c82decb2b52">IFaxTiff::get_Image</a>



<a href="https://msdn.microsoft.com/1bc248b7-a8ff-430a-9ab7-1bad9186696c">IFaxTiff::get_RawReceiveTime</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

