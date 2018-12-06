---
UID: NF:faxcom.IFaxStatus.get_Address
title: IFaxStatus::get_Address
author: windows-sdk-content
description: Retrieves the Address property for the FaxStatus object of a parent FaxPort object. The Address property is a null-terminated string that contains the destination of a fax job.
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_address_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_76er.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Address property [Fax Service], Address property [Fax Service],IFaxStatus interface, IFaxStatus interface [Fax Service],Address property, IFaxStatus.Address, IFaxStatus.get_Address, IFaxStatus::Address, IFaxStatus::get_Address, _mfax_ifaxstatus_get_address, fax._mfax_ifaxstatus_get_address, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_address_cpp, faxcom/IFaxStatus::Address, faxcom/IFaxStatus::get_Address, get_Address
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
 - IFaxStatus.Address
 - IFaxStatus.get_Address
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxStatus::get_Address


## -description


Retrieves the <b>Address</b> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>Address</b> property is a null-terminated string that contains the destination of a fax job.

This property is read-only.


## -parameters


## -remarks



The <b>IFaxStatus::get_Address</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a>



<a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a>



<a href="https://msdn.microsoft.com/823cbedb-052a-4ac1-a73c-4bbafeac2523">IFaxStatus</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

