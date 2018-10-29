---
UID: NF:faxcom.IFaxTiff.get_CallerId
title: IFaxTiff::get_CallerId
author: windows-sdk-content
description: Retrieves the CallerId property for a FaxTiff object. The CallerId property is a string that identifies the calling device that sent a specified fax file.
old-location: fax\_mfax_ifaxtiff_mfax_ifaxtiff_get_callerid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_502s.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CallerId property [Fax Service], CallerId property [Fax Service],IFaxTiff interface, IFaxTiff interface [Fax Service],CallerId property, IFaxTiff.CallerId, IFaxTiff.get_CallerId, IFaxTiff::CallerId, IFaxTiff::get_CallerId, _mfax_ifaxtiff_get_callerid, fax._mfax_ifaxtiff_get_callerid, fax._mfax_ifaxtiff_mfax_ifaxtiff_get_callerid_cpp, faxcom/IFaxTiff::CallerId, faxcom/IFaxTiff::get_CallerId, get_CallerId
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
 - IFaxTiff.CallerId
 - IFaxTiff.get_CallerId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxTiff::get_CallerId


## -description


Retrieves the <b>CallerId</b> property for a <a href="https://msdn.microsoft.com/70acd518-4058-4146-bbdf-50108d0c7e3f">FaxTiff</a> object. The <b>CallerId</b> property is a string that identifies the calling device that sent a specified fax file.

This property is read-only.


## -parameters


## -remarks



A fax client application must  set the <a href="https://msdn.microsoft.com/c993c276-eb77-4173-bfc5-0c82decb2b52">Image</a> property before retrieving another property for a <a href="https://msdn.microsoft.com/70acd518-4058-4146-bbdf-50108d0c7e3f">FaxTiff</a> object.

The <b>get_CallerId</b> method sets the <i>pVal</i> parameter to the string that identifies the calling device, if it is available. If the information is not available, the method returns "Unavailable".

The <b>CallerId</b> property is a string that identifies the calling device, if it is available. If the information is not available, <b>CallerId</b> is an empty string.

The <b>get_CallerId</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/a4c46893-502d-4d5c-a895-837cffc014e4">IFaxTiff</a>



<a href="https://msdn.microsoft.com/c993c276-eb77-4173-bfc5-0c82decb2b52">IFaxTiff::get_Image</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

