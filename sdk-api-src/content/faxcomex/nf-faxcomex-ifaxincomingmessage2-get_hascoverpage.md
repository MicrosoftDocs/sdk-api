---
UID: NF:faxcomex.IFaxIncomingMessage2.get_HasCoverPage
title: IFaxIncomingMessage2::get_HasCoverPage
author: windows-sdk-content
description: A flag that indicates whether the fax has a cover page.
old-location: fax\_mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_hascoverpage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\hascoverpage.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: HasCoverPage property [Fax Service], HasCoverPage property [Fax Service],IFaxIncomingMessage2 interface, IFaxIncomingMessage2 interface [Fax Service],HasCoverPage property, IFaxIncomingMessage2.HasCoverPage, IFaxIncomingMessage2.get_HasCoverPage, IFaxIncomingMessage2.put_HasCoverPage, IFaxIncomingMessage2::HasCoverPage, IFaxIncomingMessage2::get_HasCoverPage, IFaxIncomingMessage2::put_HasCoverPage, _mfax_faxincomingmessage.hascoverpage, fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_hascoverpage_cpp, fax._mfax_faxincomingmessage_hascoverpage, faxcomex/IFaxIncomingMessage2::HasCoverPage, faxcomex/IFaxIncomingMessage2::get_HasCoverPage, faxcomex/IFaxIncomingMessage2::put_HasCoverPage, get_HasCoverPage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxIncomingMessage2.HasCoverPage
 - IFaxIncomingMessage2.get_HasCoverPage
 - IFaxIncomingMessage2.put_HasCoverPage
 - IFaxIncomingMessage2.get_HasCoverPage
 - IFaxIncomingMessage2.put_HasCoverPage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcomex.h
: 
- IFaxIncomingMessage2.get_HasCoverPage
: 
---

# IFaxIncomingMessage2::get_HasCoverPage


## -description


A flag that indicates whether the fax has a cover page. 


<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div><div> </div>This property is read/write.


## -parameters


## -remarks



A received message has a VARIANT_FALSE value when it arrives. A <a href="https://msdn.microsoft.com/ede1c31f-e53a-4ddc-ba25-6fcadadd513a">routing assistant</a> application can set this to VARIANT_TRUE when it is reassigned. 

A change to this value is not committed to the server until <a href="https://msdn.microsoft.com/6778fa8e-6abb-40c3-92bc-cc98dd20fba4">IFaxIncomingMessage2::Save</a> is called.




## -see-also




<a href="https://msdn.microsoft.com/ee546d4c-e580-4738-a5d2-0b10c5d8a1ab">FaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/b3dc429e-1470-4e7d-8cd5-9cadb0052051">IFaxIncomingMessage2</a>
 

 

