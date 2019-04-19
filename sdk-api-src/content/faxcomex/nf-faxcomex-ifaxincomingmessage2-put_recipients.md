---
UID: NF:faxcomex.IFaxIncomingMessage2.put_Recipients
title: IFaxIncomingMessage2::put_Recipients (faxcomex.h)
author: windows-sdk-content
description: Contains the recipients associated with the inbound fax message. This property is a null-terminated string.
old-location: fax\_mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_recipients_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\recipients.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxIncomingMessage2 interface [Fax Service],Recipients property, IFaxIncomingMessage2.Recipients, IFaxIncomingMessage2.get_Recipients, IFaxIncomingMessage2.put_Recipients, IFaxIncomingMessage2::Recipients, IFaxIncomingMessage2::get_Recipients, IFaxIncomingMessage2::put_Recipients, Recipients property [Fax Service], Recipients property [Fax Service],IFaxIncomingMessage2 interface, _mfax_faxincomingmessage.recipients, fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_recipients_cpp, fax._mfax_faxincomingmessage_recipients, faxcomex/IFaxIncomingMessage2::Recipients, faxcomex/IFaxIncomingMessage2::get_Recipients, faxcomex/IFaxIncomingMessage2::put_Recipients, put_Recipients
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
 - IFaxIncomingMessage2.Recipients
 - IFaxIncomingMessage2.get_Recipients
 - IFaxIncomingMessage2.put_Recipients
 - IFaxIncomingMessage2.get_Recipients
 - IFaxIncomingMessage2.put_Recipients
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxIncomingMessage2::put_Recipients


## -description


Contains the recipients associated with the inbound fax message. This property is a null-terminated string.


<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div><div> </div>This property is read/write.


## -parameters


## -remarks



A received message starts with a null value for the recipients when it arrives. A list of recipients can be specified by a <a href="https://msdn.microsoft.com/en-us/library/Aa358860(v=VS.85).aspx">routing assistant</a> when it is reassigned.

Each recipient is identified on the pattern of &lt;DomainName&gt;\&lt;UserName&gt;. A colon ":" separates each recipient. For local users, &lt;DomainName&gt; is the local computer name.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686126(v=VS.85).aspx">FaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa358995(v=VS.85).aspx">IFaxIncomingMessage2</a>
 

 

