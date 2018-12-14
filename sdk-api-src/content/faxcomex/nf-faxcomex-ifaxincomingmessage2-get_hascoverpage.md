---
UID: NF:faxcomex.IFaxIncomingMessage2.get_HasCoverPage
title: IFaxIncomingMessage2::get_HasCoverPage
author: windows-sdk-content
description: A flag that indicates whether the fax has a cover page.
old-location: fax\_mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_hascoverpage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\hascoverpage.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
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
---

# IFaxIncomingMessage2::get_HasCoverPage


## -description


A flag that indicates whether the fax has a cover page. 


<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div><div> </div>This property is read/write.


## -parameters


## -remarks



A received message has a VARIANT_FALSE value when it arrives. A <a href="https://msdn.microsoft.com/en-us/library/Aa358860(v=VS.85).aspx">routing assistant</a> application can set this to VARIANT_TRUE when it is reassigned. 

A change to this value is not committed to the server until <a href="https://msdn.microsoft.com/en-us/library/Aa359003(v=VS.85).aspx">IFaxIncomingMessage2::Save</a> is called.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686126(v=VS.85).aspx">FaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa358995(v=VS.85).aspx">IFaxIncomingMessage2</a>
 

 

