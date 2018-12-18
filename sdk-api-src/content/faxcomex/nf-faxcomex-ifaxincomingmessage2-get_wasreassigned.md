---
UID: NF:faxcomex.IFaxIncomingMessage2.get_WasReAssigned
title: IFaxIncomingMessage2::get_WasReAssigned
author: windows-sdk-content
description: Indicates if the fax has been reassigned.
old-location: fax\_mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_wasreassigned_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\wasreassigned.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxIncomingMessage2 interface [Fax Service],WasReAssigned property, IFaxIncomingMessage2.WasReAssigned, IFaxIncomingMessage2.get_WasReAssigned, IFaxIncomingMessage2::WasReAssigned, IFaxIncomingMessage2::get_WasReAssigned, WasReAssigned property [Fax Service], WasReAssigned property [Fax Service],IFaxIncomingMessage2 interface, _mfax_faxincomingmessage.wasreassigned, fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_wasreassigned_cpp, fax._mfax_faxincomingmessage_wasreassigned, faxcomex/IFaxIncomingMessage2::WasReAssigned, faxcomex/IFaxIncomingMessage2::get_WasReAssigned, get_WasReAssigned
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
 - IFaxIncomingMessage2.WasReAssigned
 - IFaxIncomingMessage2.get_WasReAssigned
 - IFaxIncomingMessage2.get_WasReAssigned
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingMessage2::get_WasReAssigned


## -description


Indicates if the fax has been reassigned. 
<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div><div> </div>This property is read-only.


## -parameters


## -remarks



This property is always VARIANT_FALSE when the fax arrives at the server. If it is reassigned by a <a href="https://msdn.microsoft.com/en-us/library/Aa358860(v=VS.85).aspx">routing assistant</a>, the fax service sets it to VARIANT_TRUE.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686126(v=VS.85).aspx">FaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa358995(v=VS.85).aspx">IFaxIncomingMessage2</a>
 

 

