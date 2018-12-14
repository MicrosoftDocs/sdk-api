---
UID: NF:faxcomex.IFaxIncomingMessage2.get_Read
title: IFaxIncomingMessage2::get_Read
author: windows-sdk-content
description: A flag that indicates if the fax has been read.
old-location: fax\_mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_read_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\read.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxIncomingMessage2 interface [Fax Service],Read property, IFaxIncomingMessage2.Read, IFaxIncomingMessage2.get_Read, IFaxIncomingMessage2.put_Read, IFaxIncomingMessage2::Read, IFaxIncomingMessage2::get_Read, IFaxIncomingMessage2::put_Read, Read property [Fax Service], Read property [Fax Service],IFaxIncomingMessage2 interface, _mfax_faxincomingmessage.read, fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_read_cpp, fax._mfax_faxincomingmessage_read, faxcomex/IFaxIncomingMessage2::Read, faxcomex/IFaxIncomingMessage2::get_Read, faxcomex/IFaxIncomingMessage2::put_Read, get_Read
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
 - IFaxIncomingMessage2.Read
 - IFaxIncomingMessage2.get_Read
 - IFaxIncomingMessage2.put_Read
 - IFaxIncomingMessage2.get_Read
 - IFaxIncomingMessage2.put_Read
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingMessage2::get_Read


## -description


A flag that indicates if the fax has been read. 


<div class="alert"><b>Note</b>  This property is supported only in Windows Vista and later.</div><div> </div>This property is read/write.


## -parameters


## -remarks



Possible values are VARIANT_TRUE and VARIANT_FALSE.

A change to this value is not committed to the server until <a href="https://msdn.microsoft.com/en-us/library/Aa359003(v=VS.85).aspx">IFaxIncomingMessage2::Save</a> is called.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686126(v=VS.85).aspx">FaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa358995(v=VS.85).aspx">IFaxIncomingMessage2</a>
 

 

