---
UID: NF:faxcom.IFaxTiff.get_RecipientName
title: IFaxTiff::get_RecipientName
author: windows-sdk-content
description: Retrieves the RecipientName property for a FaxTiff object. The RecipientName property is a null-terminated string that contains the name of the recipient for the specified fax file.
old-location: fax\_mfax_ifaxtiff_mfax_ifaxtiff_get_recipientname_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_29b9.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IFaxTiff interface [Fax Service],RecipientName property, IFaxTiff.RecipientName, IFaxTiff.get_RecipientName, IFaxTiff::RecipientName, IFaxTiff::get_RecipientName, RecipientName property [Fax Service], RecipientName property [Fax Service],IFaxTiff interface, _mfax_ifaxtiff_get_recipientname, fax._mfax_ifaxtiff_get_recipientname, fax._mfax_ifaxtiff_mfax_ifaxtiff_get_recipientname_cpp, faxcom/IFaxTiff::RecipientName, faxcom/IFaxTiff::get_RecipientName, get_RecipientName
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
 - IFaxTiff.RecipientName
 - IFaxTiff.get_RecipientName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxTiff::get_RecipientName


## -description


Retrieves the <b>RecipientName</b> property for a <a href="https://msdn.microsoft.com/en-us/library/ms691832(v=VS.85).aspx">FaxTiff</a> object. The <b>RecipientName</b> property is a null-terminated string that contains the name of the recipient for the specified fax file.

This property is read-only.


## -parameters


## -remarks



A fax client application must  set the <a href="https://msdn.microsoft.com/c993c276-eb77-4173-bfc5-0c82decb2b52">Image</a> property before retrieving another property for a <a href="https://msdn.microsoft.com/en-us/library/ms691832(v=VS.85).aspx">FaxTiff</a> object.

The <b>get_RecipientName</b> method sets the <i>pVal</i> parameter to the name of the fax recipient, if it is available. If the information is not available, the method returns "Unavailable".

The <b>RecipientName</b> property is a string that represents the name of the fax recipient, if it is available. If the information is not available, <b>RecipientName</b> is an empty string.

The <b>get_RecipientName</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691802(v=VS.85).aspx">IFaxTiff</a>



<a href="https://msdn.microsoft.com/c993c276-eb77-4173-bfc5-0c82decb2b52">IFaxTiff::get_Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

